---
name: Run an integration preflight on a public URL
description: >-
  Given a public web page, fetch bounded integration-readiness evidence — reachability,
  robots policy, page structure, forms, integration links, security headers and a
  deterministic readiness score — and turn it into a go / no-go recommendation.
api: openapi/automation-preflight-api-preflight-openapi.json
operations:
  - analyzeIntegrationReadiness
  - health
generated: '2026-08-09'
method: generated
---

# Run an integration preflight on a public URL

Use this before committing engineering time to an integration, or to route a queue of
vendor pages into "build it", "review it by hand", or "reject it".

## Before you start

- Base URL: `https://preflight.tinyopsstudio.com`
  (the Cloudflare Workers origin
  `https://tinyops-automation-preflight.ancient-field-1495.workers.dev` answers identically).
- The target must be a **public, credential-free HTML page**. The service refuses
  private and credential-bearing targets, does not log in, does not execute
  JavaScript, and never returns raw HTML or submitted form values.
- Two tiers exist. Pick deliberately:
  - `POST /analyze` (`analyzeIntegrationReadiness`) — **no API key**, verified answering
    200 anonymously. Use this to develop against.
  - `POST /direct/analyze` (`analyzeIntegrationReadiness`, the Direct Access contract) —
    requires `X-TinyOps-API-Key`, and consumes one of 500 purchased analyses.

## Steps

1. **Confirm the service is up.** Call `health` (`GET /health`). Expect
   `{"ok": true, "status": "healthy"}`. There is no status page, so this is your only
   availability signal — check it before a batch run, not after.

2. **Submit the target.** Call `analyzeIntegrationReadiness`:

   ```
   POST /analyze
   Content-Type: application/json

   {"url": "https://example.com"}
   ```

   `url` is the only accepted property — the request schema sets
   `additionalProperties: false` and caps the URL at 2048 characters. Sending anything
   else is rejected.

3. **Check `ok` before reading anything else.** Every response carries a boolean
   discriminator. On failure you get
   `{"ok": false, "error": {"code": "...", "message": "..."}}` — not RFC 9457
   problem+json, so do not parse it as one.

4. **Read `readiness` for the decision, `target` and `robots` for the reason.**
   - `readiness.score` (0–100) and `readiness.grade` are the routing signal.
   - `readiness.components[]` tells you *which* checks earned points, so you can explain
     the score rather than just quoting it.
   - `robots.automation_restricted` and `robots.allowed` tell you whether automating
     against this site is permitted at all. Treat a restriction as a hard stop, not a
     low score.
   - `target.final_url` and `target.redirect_count` catch the case where you scored a
     redirect destination rather than the page you meant.

5. **Read `forms`, `integration_links` and `structured_data_types` for the surface.**
   These are what tell you whether an API path, a form path, or a docs path exists.
   Empty arrays are a real answer — they mean no signal was detected, not that the
   call failed.

6. **Record `analyzed_at`.** The result reflects the page as observed at that moment
   and is not a durable claim about the vendor.

## Error handling

Branch on HTTP status; `error.code` is machine-readable but its vocabulary is
unpublished, so do not hard-code codes other than the one confirmed below.

| Status | Meaning | What to do |
|---|---|---|
| 400 | Invalid or prohibited target URL | Fix the URL. Do not retry unchanged. |
| 401 | Missing/invalid/inactive key (`direct_access_key_required`) | Send `X-TinyOps-API-Key`. Direct tier only. |
| 403 | Expired key **or** target excludes the crawler | Two causes on one status — inspect `error.code`. If robots, stop; do not route around it. |
| 413 | Request or target response too large | Pick a smaller page. |
| 415 | Target is not HTML | Not analyzable. Route to manual review. |
| 422 | Target could not be resolved or fetched safely | Verify the host resolves publicly. Retry once, then give up. |
| 429 | Quota exhausted or rate limited | Read `X-TinyOps-Quota-Remaining`. If it is 0 you are out of quota, not throttled — back-off will not help. |

**There is no idempotency mechanism.** No `Idempotency-Key` header is supported. Retries
are safe only because the operation creates no server-side resource — but on the direct
tier a *successful* retry consumes another analysis. Quota is decremented on success
only, so failed calls are free.

## Quota

On the direct tier, every response carries `X-TinyOps-Quota-Limit` and
`X-TinyOps-Quota-Remaining`. Log both. A purchase is 500 successful analyses valid for
30 days from purchase — the window expires whether or not you spend the quota.
