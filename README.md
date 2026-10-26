# Ironclad (ironclad)

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
