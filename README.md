# Automation Preflight API (automation-preflight-api)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

A self-serve REST API by TinyOps Studio LLC that inspects a public URL and returns deterministic, bounded JSON integration-readiness evidence across reachability, integration surface, and readiness scoring. It rejects private/credential-bearing targets, honors robots exclusions, bounds redirects and response sizes, does not execute JavaScript, and does not return raw HTML. Three operations are published: an open POST /analyze that answers without a key, a metered POST /direct/analyze authenticated with a Gumroad license key, and POST /acceptance-pack which returns launch gates, acceptance tests, and a prioritized remediation backlog. Sold as a $19 pack of 500 analyses, as pay-as-you-go units on API.market, and per-run on AgenticTrade.

**APIs.json:** [https://automation-preflight-api.apievangelist.com/apis.yml](https://automation-preflight-api.apievangelist.com/apis.yml)

## Tags

- automation
- integration
- developer-tools
- readiness
- testing
- url-analysis
- web-scraping
- agent-tools
- quality-assurance
- site-audit

## Timestamps

- **Created:** 2026-07-29
- **Modified:** 2026-08-09

## APIs

### Automation Preflight API Acceptance Pack API

The Acceptance Pack API from Automation Preflight API — 1 operation(s) for acceptance pack.

- **Human URL:** [https://tinyopsstudio.com/automation-preflight-api](https://tinyopsstudio.com/automation-preflight-api)
- **Base URL:** `https://preflight.tinyopsstudio.com`

#### Tags

- Acceptance Pack

#### Properties

- [OpenAPI](openapi/automation-preflight-api-acceptance-pack-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/automation-preflight-api-acceptance-pack-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/automation-preflight-api-acceptance-pack-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Open A P I  Source](https://tinyopsstudio.com/assets/automation-preflight-api-openapi.json)
- [Documentation](https://tinyopsstudio.com/automation-preflight-api)

### Automation Preflight API Analyze API

The Analyze API from Automation Preflight API — 1 operation(s) for analyze.

- **Human URL:** [https://tinyopsstudio.com/automation-preflight-api](https://tinyopsstudio.com/automation-preflight-api)
- **Base URL:** `https://preflight.tinyopsstudio.com`

#### Tags

- Analyze

#### Properties

- [OpenAPI](openapi/automation-preflight-api-analyze-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/automation-preflight-api-analyze-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/automation-preflight-api-analyze-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Open A P I  Source](https://tinyopsstudio.com/assets/automation-preflight-api-openapi.json)
- [Documentation](https://tinyopsstudio.com/automation-preflight-api)

### Automation Preflight API Direct API

The Direct API from Automation Preflight API — 1 operation(s) for direct.

- **Human URL:** [https://tinyopsstudio.com/automation-preflight-api](https://tinyopsstudio.com/automation-preflight-api)
- **Base URL:** `https://preflight.tinyopsstudio.com`

#### Tags

- Direct

#### Properties

- [OpenAPI](openapi/automation-preflight-api-direct-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/automation-preflight-api-direct-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/automation-preflight-api-direct-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Open A P I  Source](https://tinyopsstudio.com/assets/automation-preflight-api-openapi.json)
- [Documentation](https://tinyopsstudio.com/automation-preflight-api)

### Automation Preflight API Health API

The Health API from Automation Preflight API — 1 operation(s) for health.

- **Human URL:** [https://tinyopsstudio.com/automation-preflight-api](https://tinyopsstudio.com/automation-preflight-api)
- **Base URL:** `https://preflight.tinyopsstudio.com`

#### Tags

- Health

#### Properties

- [OpenAPI](openapi/automation-preflight-api-health-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/automation-preflight-api-health-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/automation-preflight-api-health-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Open A P I  Source](https://tinyopsstudio.com/assets/automation-preflight-api-openapi.json)
- [Documentation](https://tinyopsstudio.com/automation-preflight-api)

## Common Properties

- [M C P Server](mcp/automation-preflight-api-mcp.yml)
- [Overlay](overlays/automation-preflight-api-direct-overlay.yaml)
- [Domain Security](security/automation-preflight-api-domain-security.yml)
- [Agentic Access](agentic-access/automation-preflight-api-agentic-access.yml)
- [Authentication](authentication/automation-preflight-api-authentication.yml)
- [Developer Portal](https://tinyopsstudio.com/product)
- [Support](https://tinyopsstudio.com/support)
- [GitHub Organization](https://github.com/tinyopsstudio)
- [Pricing](https://api.market/store/tinyopsstudio/automation-preflight)
- [Sign Up](https://tinyopsstudio.gumroad.com/l/automation-preflight-api-500)
- [Terms of Service](https://tinyopsstudio.com/terms)
- [Privacy Policy](https://tinyopsstudio.com/privacy)
- [Agent Card](a2a/automation-preflight-api-a2a.yml)
- [Well Known](well-known/automation-preflight-api-well-known.yml)
- [L L Ms Txt](llms/automation-preflight-api-llms.txt)
- [L L Ms Txt  Source](https://tinyopsstudio.com/llms.txt)
- [Agent Skill](skills/_index.yml)
- [Conventions](conventions/automation-preflight-api-conventions.yml)
- [Error Catalog](errors/automation-preflight-api-problem-types.yml)
- [Lifecycle](lifecycle/automation-preflight-api-lifecycle.yml)
- [Conformance](conformance/automation-preflight-api-conformance.yml)
- [Data Model](data-model/automation-preflight-api-data-model.yml)
- [Rate Limits](rate-limits/automation-preflight-api-rate-limits.yml)
- [Plans](plans/automation-preflight-api-plans.yml)
- [Sandbox](sandbox/automation-preflight-api-sandbox.yml)
- [Examples](examples/automation-preflight-api-analyze-example.json)
- [Examples](examples/automation-preflight-api-health-and-errors-example.json)

## Maintainers

**FN:** TinyOps Studio LLC
**Email:** support@tinyopsstudio.com
**URL:** https://tinyopsstudio.com
