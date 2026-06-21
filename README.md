# Slab (slab)

Slab is an internal knowledge base and team wiki for the modern workplace, pairing a clean editor and fast search with dozens of integrations. Slab exposes a single GraphQL API at https://api.slab.com/v1/graphql for programmatic access to posts, topics, users, and organization data, available to Business and Enterprise customers.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/slab/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/slab/refs/heads/main/apis.yml)

## Tags

- Knowledge Base
- Wiki
- Documentation
- Collaboration
- GraphQL

## Timestamps

- **Created:** 2026-06-21
- **Modified:** 2026-06-21

## APIs

### Slab Posts

Query and update knowledge base posts through the Slab GraphQL API - fetch a post by ID, search posts across the workspace with cursor-based pagination, list posts within a topic or across the organization, and update post content using the Quill Delta rich-text format.

- **Human URL:** [https://help.slab.com/en/articles/6545629-developer-tools-api-webhooks](https://help.slab.com/en/articles/6545629-developer-tools-api-webhooks)
- **Base URL:** `https://api.slab.com/v1/graphql`

#### Tags

- Posts
- Content
- GraphQL

#### Properties

- [Documentation](https://help.slab.com/en/articles/6545629-developer-tools-api-webhooks)
- [API Reference](https://studio.apollographql.com/public/Slab/variant/current/schema/reference)
- [GraphQL](graphql/slab-graphql.md) — [GraphQL Schema](https://spec.graphql.org/)
- [OpenAPI](openapi/slab-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/slab.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/slab.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Slab Topics

Read the topic hierarchy used to organize content in a Slab workspace, resolve a topic by ID, and list the posts nested within a topic. Topics are the primary structure for grouping and navigating knowledge base content.

- **Human URL:** [https://help.slab.com/en/articles/6545629-developer-tools-api-webhooks](https://help.slab.com/en/articles/6545629-developer-tools-api-webhooks)
- **Base URL:** `https://api.slab.com/v1/graphql`

#### Tags

- Topics
- Organization
- GraphQL

#### Properties

- [Documentation](https://help.slab.com/en/articles/6545629-developer-tools-api-webhooks)
- [API Reference](https://studio.apollographql.com/public/Slab/variant/current/schema/reference)
- [GraphQL](graphql/slab-graphql.md) — [GraphQL Schema](https://spec.graphql.org/)
- [OpenAPI](openapi/slab-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/slab.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/slab.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Slab Users

Resolve the members of a Slab organization through the GraphQL API - look up a user by ID and read profile fields such as name and email, used to attribute authorship and map activity to people.

- **Human URL:** [https://help.slab.com/en/articles/6545629-developer-tools-api-webhooks](https://help.slab.com/en/articles/6545629-developer-tools-api-webhooks)
- **Base URL:** `https://api.slab.com/v1/graphql`

#### Tags

- Users
- Members
- GraphQL

#### Properties

- [Documentation](https://help.slab.com/en/articles/6545629-developer-tools-api-webhooks)
- [API Reference](https://studio.apollographql.com/public/Slab/variant/current/schema/reference)
- [GraphQL](graphql/slab-graphql.md) — [GraphQL Schema](https://spec.graphql.org/)
- [OpenAPI](openapi/slab-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/slab.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/slab.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Slab Organization

Read top-level organization (workspace) context through the Slab GraphQL API, including the organization entry point that scopes posts, topics, and users. API responses are bounded by what the Slab Bot user can access in the workspace.

- **Human URL:** [https://help.slab.com/en/articles/6545629-developer-tools-api-webhooks](https://help.slab.com/en/articles/6545629-developer-tools-api-webhooks)
- **Base URL:** `https://api.slab.com/v1/graphql`

#### Tags

- Organization
- Account
- GraphQL

#### Properties

- [Documentation](https://help.slab.com/en/articles/6545629-developer-tools-api-webhooks)
- [API Reference](https://studio.apollographql.com/public/Slab/variant/current/schema/reference)
- [GraphQL](graphql/slab-graphql.md) — [GraphQL Schema](https://spec.graphql.org/)
- [OpenAPI](openapi/slab-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/slab.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/slab.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/slab)
- [LinkedIn](https://www.linkedin.com/company/slab-inc)
- [Website](https://slab.com/)
- [Documentation](https://help.slab.com/en/articles/6545629-developer-tools-api-webhooks)
- [Plans](plans/slab-plans-pricing.yml)
- [Rate Limits](rate-limits/slab-rate-limits.yml)
- [Fin Ops](finops/slab-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
