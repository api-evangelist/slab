# Slab (slab)

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
