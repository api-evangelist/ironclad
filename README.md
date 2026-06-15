# Ironclad (ironclad)

Ironclad is the enterprise contract lifecycle management (CLM) platform used by legal, sales, procurement, and finance teams to draft, negotiate, approve, sign, store, and analyze contracts at scale. The platform combines a no-code Workflow Designer, AI-powered Jurist agentic assistant (contract review, redlining, drafting, repository search), a Records repository with smart import and metadata extraction, Clickwrap for online acceptance, and deep integrations with Salesforce, Microsoft 365, Slack, Workday, ServiceNow, Jira, HubSpot, NetSuite, Dynamics 365, and Power Automate. Ironclad publishes three first-party OpenAPI 3.1 specifications (Public API, OAuth 2.0, SCIM 2.0) plus the Clickwrap REST/JS surface, supports regional NA1/EU1 hosting, OAuth 2.0 with scoped tokens, SCIM-based provisioning, and event-driven webhooks. Ironclad reported surpassing $200M in ARR in February 2026.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/ironclad/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/ironclad/refs/heads/main/apis.yml)

## Scope

- **Access:** 3rd-Party

## Tags

- Contract Lifecycle Management
- CLM
- Contracts
- Legal Tech
- LegalOps
- Enterprise
- Workflows
- eSignature
- Clickwrap
- AI
- OAuth
- SCIM
- Webhooks

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Ironclad Public API

The Ironclad Public API exposes contract lifecycle management primitives — Workflows (contract authoring, approvals, signature packets, comments, signers), Records (the executed contract repository with metadata, attachments, smart-import predictions), Entities (counterparties and parties referenced across workflows and records), Obligations (post-signature commitments derived from contracts), Webhooks (event-driven integration into downstream systems), Exports (bulk data warehouse pulls), and Conversational Search (Jurist-powered natural-language queries over the contract repository). REST/JSON over HTTPS with OAuth 2.0 (Authorization Code and Client Credentials) and bearer-token authentication; OpenAPI 3.1; regional NA1, EU1, and demo servers.

- **Human URL:** [https://developer.ironcladapp.com/reference/getting-started-api](https://developer.ironcladapp.com/reference/getting-started-api)
- **Base URL:** `https://na1.ironcladapp.com/public/api/v1`

#### Tags

- Contracts
- Contract Lifecycle Management
- CLM
- Workflows
- Records
- Entities
- Obligations
- Webhooks
- Exports

#### Properties

- [Documentation](https://developer.ironcladapp.com/reference/getting-started-api)
- [Authentication](https://developer.ironcladapp.com/reference/authenticate-a-request)
- [Rate Limits](https://developer.ironcladapp.com/reference/clm-api-rate-limits)
- [OpenAPI](openapi/ironclad-public-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ironclad-public-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ironclad-public-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/ironclad-workflow-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/ironclad-record-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/ironclad-entity-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/ironclad-webhook-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/ironclad-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Example](examples/ironclad-launch-workflow-example.json)
- [Example](examples/ironclad-create-record-example.json)
- [Example](examples/ironclad-create-webhook-example.json)
- [Example](examples/ironclad-conversational-search-example.json)

### Ironclad OAuth 2.0 API

OAuth 2.0 endpoints for delegated and machine-to-machine access to the Ironclad Public API. Supports the Authorization Code grant (with PKCE for public clients) and the Client Credentials grant for server-to-server integrations. Exposes /authorize, /token, /userinfo, and /company-info; scopes follow the `public.{resource}.{action}` convention (e.g., `public.workflows.readWorkflows`, `public.records.createRecords`).

- **Human URL:** [https://developer.ironcladapp.com/reference/authentication-api](https://developer.ironcladapp.com/reference/authentication-api)
- **Base URL:** `https://na1.ironcladapp.com/oauth`

#### Tags

- OAuth
- Authentication
- Authorization
- Identity

#### Properties

- [Documentation](https://developer.ironcladapp.com/reference/authentication-api)
- [Documentation](https://developer.ironcladapp.com/reference/authorization-code-grant)
- [Documentation](https://developer.ironcladapp.com/reference/client-credentials-grant)
- [Documentation](https://developer.ironcladapp.com/reference/register-oauth-client)
- [Documentation](https://developer.ironcladapp.com/reference/guidance-for-oauth-migration)
- [OpenAPI](openapi/ironclad-oauth-20-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ironclad-oauth-20-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ironclad-oauth-20-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ironclad SCIM 2.0 API

SCIM 2.0 endpoints for Just-in-Time and bulk provisioning of Ironclad users and groups from an upstream identity provider (Okta, Azure AD, OneLogin, etc.). Implements /Users, /Groups, and /Schemas with standard SCIM semantics — list/get/create/replace/delete plus PATCH for partial updates and group-membership edits. Enables SSO-aligned lifecycle management and role-based access.

- **Human URL:** [https://developer.ironcladapp.com/reference/retrieve-all-users](https://developer.ironcladapp.com/reference/retrieve-all-users)
- **Base URL:** `https://na1.ironcladapp.com/scim/v2`

#### Tags

- SCIM
- Identity
- User Provisioning
- Groups
- Directory

#### Properties

- [Documentation](https://developer.ironcladapp.com/reference/retrieve-all-users)
- [OpenAPI](openapi/ironclad-scim-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ironclad-scim-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ironclad-scim-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/ironclad-user-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Ironclad Clickwrap API

The Ironclad Clickwrap (formerly PactSafe) API delivers programmatic clickwrap and browsewrap acceptance tracking for online agreements — terms of service, privacy policies, EULAs, and checkout-flow agreements. Comprises a JavaScript library (PS.js) for rendering and capturing acceptance events, an Activity API for sending acceptance/visit/displayed/agreed events server-side, and a REST API for managing Sites, Groups, Contracts, and Signer records. Powers in-product acceptance for SaaS sign-ups, checkout pages, mobile apps, and embedded forms.

- **Human URL:** [https://clickwrap-developer.ironcladapp.com/docs/getting-started](https://clickwrap-developer.ironcladapp.com/docs/getting-started)
- **Base URL:** `https://pactsafe.io`

#### Tags

- Clickwrap
- Acceptance
- Online Agreements
- PactSafe

#### Properties

- [Documentation](https://clickwrap-developer.ironcladapp.com/docs/getting-started)
- [Documentation](https://clickwrap-developer.ironcladapp.com/docs/activity-api)
- [SDK](https://clickwrap-developer.ironcladapp.com/docs/javascript-library-getting-started)
- [Authentication](https://clickwrap-developer.ironcladapp.com/docs/getting-your-access-token)
- [Postman Collection](collections/ironclad-oauth-20-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ironclad-oauth-20-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/ironclad-public-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ironclad-public-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/ironclad-scim-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ironclad-scim-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Portal](https://developer.ironcladapp.com/)
- [Documentation](https://developer.ironcladapp.com/reference/getting-started-api)
- [Documentation](https://developer.ironcladapp.com/docs/getting-started)
- [API Reference](https://developer.ironcladapp.com/reference)
- [Authentication](https://developer.ironcladapp.com/reference/authentication-api)
- [Rate Limits](https://developer.ironcladapp.com/reference/clm-api-rate-limits)
- [Changelog](https://developer.ironcladapp.com/changelog/release-notes)
- [Status Page](https://status.ironcladapp.com/)
- [GitHub Organization](https://github.com/ironclad)
- [SDK](https://github.com/ironclad/rivet)
- [LinkedIn](https://www.linkedin.com/company/ironclad-inc-)
- [Pricing](https://ironcladapp.com/pricing)
- [Terms of Service](https://ironcladapp.com/master-subscription-agreement/)
- [Privacy Policy](https://ironcladapp.com/privacy/)
- [Support](https://support.ironcladapp.com/)
- [Blog](https://ironcladapp.com/journal/)
- [Plans](plans/ironclad-plans-pricing.yml)
- [Rate Limits](rate-limits/ironclad-rate-limits.yml)
- [Fin Ops](finops/ironclad-finops.yml)
- [Spectral Rules](rules/ironclad-rules.yml)
- [Vocabulary](vocabulary/ironclad-vocabulary.yml)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)
- [Solutions](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** http://kinlane.com
