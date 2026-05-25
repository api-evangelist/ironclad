# Ironclad (ironclad)

Ironclad is the enterprise contract lifecycle management (CLM) platform used by legal, sales, procurement, and finance teams to draft, negotiate, approve, sign, store, and analyze contracts at scale. The platform combines a no-code Workflow Designer, AI-powered Jurist agentic assistant (contract review, redlining, drafting, repository search), a Records repository with smart import and metadata extraction, Clickwrap for online acceptance, and deep integrations with Salesforce, Microsoft 365, Slack, Workday, ServiceNow, Jira, HubSpot, NetSuite, Dynamics 365, and Power Automate. Ironclad publishes three first-party OpenAPI 3.1 specifications (Public API, OAuth 2.0, SCIM 2.0) plus the Clickwrap REST/JS surface, supports regional NA1/EU1 hosting, OAuth 2.0 with scoped tokens, SCIM-based provisioning, and event-driven webhooks. Ironclad reported surpassing $200M in ARR in February 2026.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/ironclad/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

- Contract Lifecycle Management, CLM, Contracts, Legal Tech, LegalOps, Enterprise, Workflows, eSignature, Clickwrap, AI, OAuth, SCIM, Webhooks

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

| API | Base URL | Operations | OpenAPI |
|---|---|---|---|
| Ironclad Public API | `https://na1.ironcladapp.com/public/api/v1` (NA1) / `https://eu1.ironcladapp.com/public/api/v1` (EU1) | 80 | [openapi/ironclad-public-api-openapi.yml](openapi/ironclad-public-api-openapi.yml) |
| Ironclad OAuth 2.0 API | `https://na1.ironcladapp.com/oauth` | 4 | [openapi/ironclad-oauth-20-api-openapi.yml](openapi/ironclad-oauth-20-api-openapi.yml) |
| Ironclad SCIM 2.0 API | `https://na1.ironcladapp.com/scim/v2` | 14 | [openapi/ironclad-scim-api-openapi.yml](openapi/ironclad-scim-api-openapi.yml) |
| Ironclad Clickwrap API | `https://pactsafe.io` | REST + JS library | See [Clickwrap developer portal](https://clickwrap-developer.ironcladapp.com/) |

## Public API — Resource Surfaces

| Tag | Operations | Capability |
|---|---|---|
| Workflows | 43 | [capabilities/workflows.yaml](capabilities/workflows.yaml) |
| Records | 17 | [capabilities/records.yaml](capabilities/records.yaml) |
| Entities | 6 | [capabilities/entities.yaml](capabilities/entities.yaml) |
| Webhooks | 6 | [capabilities/webhooks.yaml](capabilities/webhooks.yaml) |
| Obligations | 4 | [capabilities/obligations.yaml](capabilities/obligations.yaml) |
| Exports | 3 | [capabilities/exports.yaml](capabilities/exports.yaml) |
| Search | 1 | [capabilities/search.yaml](capabilities/search.yaml) |
| OAuth | 4 | [capabilities/oauth.yaml](capabilities/oauth.yaml) |
| SCIM | 14 | [capabilities/scim.yaml](capabilities/scim.yaml) |

## Authentication

- **Authorization Code grant** — Delegated user access via `/oauth/authorize` and `/oauth/token`. Supports PKCE.
- **Client Credentials grant** — Machine-to-machine via `/oauth/token` with `grant_type=client_credentials`.
- **Scopes** — `public.{resource}.{action}` (e.g., `public.workflows.readWorkflows`, `public.records.createRecords`, `public.webhooks.createWebhooks`).
- **Legacy access tokens** — Long-lived tokens are being migrated to OAuth 2.0; see the [OAuth migration guide](https://developer.ironcladapp.com/reference/guidance-for-oauth-migration).

## Regions

- `na1` — North America production (`https://na1.ironcladapp.com`)
- `eu1` — EU production (`https://eu1.ironcladapp.com`)
- `demo` — Demo / sandbox (`https://demo.ironcladapp.com`)

## Artifacts

| Type | Folder | Files |
|---|---|---|
| OpenAPI | [`openapi/`](openapi/) | 3 specs (Public API, OAuth 2.0, SCIM 2.0) — OpenAPI 3.1.0 |
| Naftiko Capabilities | [`capabilities/`](capabilities/) | 9 capabilities, one per Ironclad business surface |
| JSON Schema | [`json-schema/`](json-schema/) | Workflow, Record, Entity, Webhook, User |
| JSON-LD | [`json-ld/`](json-ld/) | `ironclad-context.jsonld` — schema.org-aligned linked-data context |
| Examples | [`examples/`](examples/) | Launch workflow, create record, create webhook, conversational search |
| Spectral Rules | [`rules/`](rules/) | `ironclad-rules.yml` — server, tagging, naming, error, security conventions |
| Vocabulary | [`vocabulary/`](vocabulary/) | `ironclad-vocabulary.yml` — concepts, operations, capabilities |
| Plans | [`plans/`](plans/) | `ironclad-plans-pricing.yml` — API Commons Plans 0.1 |
| Rate Limits | [`rate-limits/`](rate-limits/) | `ironclad-rate-limits.yml` — API Commons Rate Limits 0.1 |
| FinOps | [`finops/`](finops/) | `ironclad-finops.yml` — FinOps Framework + FOCUS 1.3 |

## Common Resources

- [Developer Portal](https://developer.ironcladapp.com/)
- [API Reference](https://developer.ironcladapp.com/reference)
- [Getting Started](https://developer.ironcladapp.com/docs/getting-started)
- [Authentication](https://developer.ironcladapp.com/reference/authentication-api)
- [CLM API Rate Limits](https://developer.ironcladapp.com/reference/clm-api-rate-limits)
- [Release Notes](https://developer.ironcladapp.com/changelog/release-notes)
- [Status](https://status.ironcladapp.com/)
- [Pricing](https://ironcladapp.com/pricing)
- [GitHub](https://github.com/ironclad) — includes [Rivet](https://github.com/ironclad/rivet) (open-source visual AI programming environment)
- [Support](https://support.ironcladapp.com/)
- [Blog (Ironclad Journal)](https://ironcladapp.com/journal/)
- [LinkedIn](https://www.linkedin.com/company/ironclad-inc-)
- [Clickwrap Developer Portal](https://clickwrap-developer.ironcladapp.com/)

## Solutions

- **Ironclad CLM Platform** — Workflows, records, repository, eSignature.
- **Jurist AI Assistant** — Agentic contract review, drafting, redlining, summarization, conversational search.
- **Ironclad Clickwrap** — Online-agreement acceptance (PS.js + Activity API + REST API).
- **Security & Data Pro** — Per-tenant encryption with HYOK (Antimatter or GCP).
- **Ironclad Insights** — Contract reporting and BI.

## Features

- AI-Powered Contract Review (Jurist)
- No-Code Workflow Designer
- Smart Import (ML metadata extraction from legacy PDFs)
- Repository and Records (versioned attachments, schemas, full-text + conversational search)
- Webhooks (workflow / record / entity events)
- Data Exports (Snowflake, BigQuery, Databricks, Redshift)
- Clickwrap and Browsewrap (PS.js, Activity API, REST API)
- Entity Management (counterparties, parties, relationships)
- Obligation Tracking (renewals, SLAs, payment milestones, regulatory deadlines)
- OAuth 2.0 (Authorization Code + Client Credentials)
- SCIM 2.0 provisioning (Okta, Azure AD, OneLogin, etc.)
- Regional hosting (NA1, EU1) for data-residency compliance
- Per-Tenant Encryption / HYOK

## Use Cases

- Sales Contract Automation (Salesforce → NDA / MSA / Order Form workflows)
- Procurement Lifecycle (Workday / NetSuite / Coupa / ServiceNow integration)
- Legal Operations (matter management, clause libraries, AI first-pass review)
- HR / Employment Agreements (offer letters, NDAs, separation agreements)
- Repository Migration (legacy-PDF Smart Import)
- Online Agreement Acceptance (SaaS sign-up, checkout, policy acknowledgement)
- Compliance and Obligation Management (renewal dates, SLAs)
- AI-Augmented Repository Search (natural-language contract queries via Jurist)

## Integrations

Salesforce · Microsoft Word · Microsoft 365 / Power Automate · Microsoft Dynamics 365 · ServiceNow · Slack · HubSpot · Jira · NetSuite · Zapier · MuleSoft · Box · Snowflake / BigQuery / Databricks / Redshift

---

*This profile is built and maintained by [API Evangelist](https://apievangelist.com). The OpenAPI specs in this repository are downloaded directly from Ironclad's developer portal at `https://developer.ironcladapp.com/openapi`.*
