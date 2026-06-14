# Ironclad GraphQL Schema

## Overview

This conceptual GraphQL schema represents the Ironclad digital contracting platform API surface. Ironclad's public REST API (base URL: `https://na1.ironcladapp.com/public/api/v1`) exposes contract lifecycle management primitives including Workflows, Records, Entities, Obligations, Webhooks, Exports, and Conversational Search. This GraphQL schema models the same domain as a typed graph to support client-driven queries, reduced over-fetching, and nested relationship traversal in a single request.

## Source API

- **Provider**: Ironclad
- **REST Reference**: https://developer.ironcladapp.com/reference
- **Base URL**: https://na1.ironcladapp.com/public/api/v1
- **Auth**: OAuth 2.0 (Authorization Code, Client Credentials) with bearer tokens
- **Regions**: NA1, EU1, Demo

## Schema File

See `ironclad-schema.graphql` for the full type definitions.

## Key Domain Objects

### Workflows

Workflows are the core contracting unit in Ironclad — a workflow represents a contract in progress, moving through steps (form fill, review, approval, signature). Each workflow is launched from a template (WorkflowType) and carries structured metadata, documents, approvers, signers, and comments.

**Types**: `Workflow`, `WorkflowDetails`, `WorkflowType`, `WorkflowStatus`, `WorkflowStep`, `StepType`

### Documents

Documents are the contract files (Word, PDF) attached to a workflow. Ironclad tracks versions and manages the signature packet ordering. Documents can be previewed, downloaded, and reordered within the signature packet.

**Types**: `Document`, `DocumentDetails`, `DocumentVersion`, `DocumentStatus`

### Templates

Templates (called "launch schemas" in the REST API) define the structure of a workflow — fields, conditional logic, and document slots. They drive the no-code Workflow Designer experience.

**Types**: `Template`, `TemplateDetails`, `TemplateField`

### Approvals and Signatures

Ironclad routes contracts through configurable approval steps and then manages an eSignature packet. Approvers have roles, signers have an order, and signatures carry status.

**Types**: `Approver`, `ApproverRole`, `Signer`, `SignerDetails`, `SignerOrder`, `Signature`, `SignatureDetails`, `SignatureStatus`, `Approval`, `ApprovalDetails`

### Contracts and Records

Once executed, a workflow becomes a Record in the repository. Records carry contract metadata, attachments, and structured fields. Smart Import can ingest legacy PDFs and predict metadata.

**Types**: `Contract`, `ContractDetails`, `ContractType`, `ContractStatus`, `ContractTerms`, `ContractParty`, `PartyDetails`, `PartyRole`, `Counterparty`, `CounterpartyDetails`

### Metadata and Clauses

Both workflows and records carry flexible metadata fields. Clauses represent contract provisions that can be extracted, tracked, and compared.

**Types**: `Metadata`, `MetadataField`, `MetadataValue`, `Clause`, `ClauseDetails`, `ClauseType`

### Reviews and Reminders

Workflows pass through review steps. Reminders can be scheduled for upcoming renewal, expiration, or obligation dates.

**Types**: `Review`, `ReviewDetails`, `ReviewStatus`, `ReviewComment`, `Reminder`, `ReminderDetails`

### Renewals and Expirations

Post-execution, Ironclad tracks contract renewal terms and expiration milestones derived from metadata.

**Types**: `Renewal`, `RenewalDetails`, `ExpirationDetails`

### Repository and Search

The Records repository supports folder organization and full-text plus conversational (Jurist AI) search across the contract corpus.

**Types**: `Repository`, `RepositoryFolder`, `SearchQuery`, `SearchResults`

### Users, Teams, and Organization

Ironclad models users with roles, grouped into teams, under a single organization tenant. SCIM 2.0 provisioning manages the user lifecycle.

**Types**: `User`, `UserDetails`, `UserRole`, `Team`, `TeamDetails`, `Organization`

### Auth and Webhooks

API keys and OAuth tokens provide programmatic access. Webhooks deliver event-driven notifications to downstream systems for workflow, record, and entity events.

**Types**: `APIKey`, `Token`, `Webhook`, `WebhookEvent`

## Queries

- `workflow(id: ID!)` — fetch a single workflow by ID
- `workflows(status: WorkflowStatus, templateId: ID, limit: Int, offset: Int)` — list workflows with filters
- `workflowTypes(limit: Int, offset: Int)` — list available workflow templates/schemas
- `document(id: ID!, workflowId: ID!)` — fetch a document attached to a workflow
- `contract(id: ID!)` — fetch a contract record from the repository
- `contracts(type: ContractType, status: ContractStatus, counterpartyId: ID, limit: Int, offset: Int)` — list contract records
- `counterparty(id: ID!)` — fetch a counterparty entity
- `counterparties(limit: Int, offset: Int)` — list counterparty entities
- `searchContracts(query: SearchQuery!)` — conversational/full-text search over the repository
- `user(id: ID!)` — fetch a user
- `users(teamId: ID, role: UserRole, limit: Int, offset: Int)` — list users
- `team(id: ID!)` — fetch a team
- `organization` — fetch the current organization tenant
- `webhook(id: ID!)` — fetch a webhook subscription
- `webhooks(limit: Int, offset: Int)` — list webhook subscriptions

## Mutations

- `launchWorkflow(input: LaunchWorkflowInput!)` — create and launch a new workflow from a template
- `updateWorkflowMetadata(id: ID!, metadata: [MetadataValueInput!]!)` — update workflow metadata fields
- `cancelWorkflow(id: ID!, reason: String)` — cancel an in-progress workflow
- `pauseWorkflow(id: ID!, comment: String)` — pause a workflow at the current step
- `resumeWorkflow(id: ID!, comment: String)` — resume a paused workflow
- `approveWorkflow(id: ID!, roleId: ID!, comment: String)` — approve the current approval step
- `sendForSignature(workflowId: ID!, scheduledAt: String)` — send the signature packet to signers
- `addSigner(workflowId: ID!, signer: SignerInput!)` — add a signer to the signature packet
- `createContract(input: CreateContractInput!)` — create a new contract record in the repository
- `updateContract(id: ID!, input: UpdateContractInput!)` — update contract record metadata
- `createWebhook(input: CreateWebhookInput!)` — register a new webhook subscription
- `updateWebhook(id: ID!, input: UpdateWebhookInput!)` — update webhook events or target URL
- `deleteWebhook(id: ID!)` — remove a webhook subscription

## Notes

- This schema is a conceptual GraphQL representation derived from the Ironclad REST API surface documented at https://developer.ironcladapp.com/reference.
- Ironclad does not publish a native GraphQL endpoint; this schema is suitable for tooling, documentation generation, API gateway layers, or client SDK generation.
- Regional variants (eu1, demo) can be modeled via a `region` scalar or server-selection mechanism.
- Pagination follows a limit/offset model matching the REST API conventions.
