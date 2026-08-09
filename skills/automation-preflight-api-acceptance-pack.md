---
name: Build an automation acceptance pack for a target site
description: >-
  Turn a public URL plus a stated objective into an implementation-ready handoff:
  preflight evidence, launch gates, acceptance tests, and a prioritized remediation
  backlog.
api: openapi/automation-preflight-api-preflight-openapi.json
operations:
  - buildAutomationAcceptancePack
  - analyzeIntegrationReadiness
generated: '2026-08-09'
method: generated
---

# Build an automation acceptance pack

Use this when a preflight has already told you a target is worth pursuing and you now
need something an implementer can act on — gates, tests, and a ranked backlog rather
than raw evidence.

## Before you start

- Base URL: `https://preflight.tinyopsstudio.com`.
- This is the packaged, higher-value operation. It is sold per run ($25) on
  AgenticTrade; the endpoint itself declares no security requirement in the published
  contract.
- Run the cheaper preflight first (see the integration-preflight skill). If
  `readiness.grade` is very low or `robots.automation_restricted` is true, stop — an
  acceptance pack for a target you may not automate is wasted.

## Steps

1. **State the objective in words.** Call `buildAutomationAcceptancePack`:

   ```
   POST /acceptance-pack
   Content-Type: application/json

   {
     "url": "https://example.com/signup",
     "objective": "Automate new-customer signup and capture the confirmation reference"
   }
   ```

   `url` is required; `objective` is optional and capped at 500 characters. The request
   schema is `additionalProperties: false` — those two properties are all it accepts.

   Write the objective as the outcome you need, not the tool you plan to use. It shapes
   the gates and tests that come back.

2. **Check `ok` first**, exactly as with the preflight operation. The error envelope and
   status codes are the same set (400 / 403 / 415 / 422 / 429), minus the key-specific
   401.

3. **Use the three sections for three different jobs.**
   - **Launch gates** — the conditions that must hold before you ship. Treat these as
     blocking, and put them in front of a human.
   - **Acceptance tests** — the checks that prove the automation works. These belong in
     your test suite, not in a document.
   - **Remediation backlog** — already prioritized. Work it top-down.

4. **Re-run after remediation.** The pack describes the page as observed at
   `analyzed_at`. Once the backlog is worked, run it again and diff, rather than
   assuming the gates now pass.

## Boundaries to respect

The service is explicit that this is **public-page preflight, not authenticated
automation and not a security certification**. A clean pack does not prove a
third-party integration works — it proves the public surface is consistent with one.
Never present the output as a security assessment of the target.

## Error handling

Identical to the preflight skill, including the overloaded 403 (expired access *or*
robots exclusion) and the unpublished `error.code` vocabulary. There is no
idempotency key; a retry re-runs the analysis.
