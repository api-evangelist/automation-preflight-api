# Automation Preflight API (automation-preflight-api)

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
