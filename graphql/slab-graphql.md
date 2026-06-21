# Slab GraphQL Schema

Conceptual GraphQL schema for the [Slab](https://slab.com/) knowledge base and team wiki platform.
Covers the single **GraphQL API** served at `https://api.slab.com/v1/graphql`.

- Developer docs: <https://help.slab.com/en/articles/6545629-developer-tools-api-webhooks>
- Schema reference (Apollo Studio, public): <https://studio.apollographql.com/public/Slab/variant/current/schema/reference>
- GitHub: <https://github.com/slab>

---

## Overview

Slab exposes a single GraphQL endpoint for programmatic access to a workspace's posts,
topics, users, and organization. All operations are performed by issuing an HTTP `POST` to
`https://api.slab.com/v1/graphql` with a JSON body containing `query` and optional
`variables`, and an `Authorization` header carrying the API token.

The API is available to customers on the **Business** or **Enterprise** plan. The token is
generated in Slab under **Team Settings → Developer Tools**. API responses are scoped to
what the **Slab Bot** user can access; content in private topics that Slab Bot is not a
member of is not returned.

Post content is represented in the [Quill](https://github.com/slab/quill) **Delta**
rich-text format, the same open-source document model Slab maintains for its editor.

> The schema below is a **representative** SDL reconstructed from Slab's public developer
> documentation, the public Apollo Studio schema reference, and community integrations
> (operation and field names are noted as representative rather than copied from a published
> SDL file).

---

## Transport

| Property | Value |
|----------|-------|
| Endpoint | `https://api.slab.com/v1/graphql` |
| Method | `POST` |
| Content-Type | `application/json` |
| Auth header | `Authorization: <token>` (Bearer token from Team Settings → Developer Tools) |
| Plan requirement | Business or Enterprise |
| Access scope | Bounded by Slab Bot user permissions |

---

## Schema file

See [`slab-schema.graphql`](./slab-schema.graphql) for the full representative schema.

---

## Type inventory

### Scalars
| Scalar | Purpose |
|--------|---------|
| `ID` | Opaque object identifiers |
| `DateTime` | ISO-8601 timestamps (e.g. `insertedAt`, `updatedAt`) |
| `JSON` | Quill Delta rich-text content payloads |

### Object types

#### Organization
- `Organization` — top-level workspace; entry point that scopes posts, topics, and users

#### Post
- `Post` — a knowledge base post with title, Quill Delta content, version, timestamps, owner, and topics
- `PostConnection` — cursor-paginated list of posts (`edges`, `pageInfo`)
- `PostEdge` — `node` + `cursor` wrapper for a post
- `PageInfo` — `hasNextPage`, `hasPreviousPage`, `startCursor`, `endCursor`

#### Topic
- `Topic` — a content grouping with name, description, hierarchy, and nested posts
- `TopicConnection` — cursor-paginated list of topics
- `TopicEdge` — `node` + `cursor` wrapper for a topic

#### User
- `User` — an organization member with name and email

---

## Query operations

| Operation | Purpose |
|-----------|---------|
| `organization` | Fetch the current workspace/organization context |
| `post(id: ID!)` | Retrieve a single post by ID, including Quill Delta content |
| `posts(first, after)` | List posts across the organization with cursor pagination |
| `search(query, first, after)` | Search posts across the workspace |
| `topic(id: ID!)` | Retrieve a single topic by ID |
| `topics(first, after)` | List topics in the organization |
| `user(id: ID!)` | Retrieve a single user by ID |
| `users(first, after)` | List users (members) in the organization |

## Mutation operations

| Operation | Purpose |
|-----------|---------|
| `updatePost(id, content)` | Update a post's content using the Quill Delta format |

---

## Query examples

### Fetch a post by ID

```graphql
query GetPost($id: ID!) {
  post(id: $id) {
    id
    title
    content
    version
    insertedAt
    updatedAt
    topics {
      id
      name
    }
  }
}
```

### List posts across the organization (cursor pagination)

```graphql
query GetOrganizationPosts($first: Int!, $after: String) {
  posts(first: $first, after: $after) {
    edges {
      node {
        id
        title
        insertedAt
        updatedAt
      }
      cursor
    }
    pageInfo {
      hasNextPage
      endCursor
    }
  }
}
```

### Search posts

```graphql
query SearchPosts($query: String!, $first: Int!) {
  search(query: $query, first: $first) {
    edges {
      node {
        id
        title
      }
    }
    pageInfo {
      hasNextPage
      endCursor
    }
  }
}
```

### List posts within a topic

```graphql
query GetTopicPosts($id: ID!) {
  topic(id: $id) {
    id
    name
    posts(first: 50) {
      edges {
        node {
          id
          title
        }
      }
      pageInfo {
        hasNextPage
        endCursor
      }
    }
  }
}
```

### Resolve a user

```graphql
query GetUser($id: ID!) {
  user(id: $id) {
    id
    name
    email
  }
}
```

### Update post content (Quill Delta)

```graphql
mutation UpdatePostContent($id: ID!, $content: JSON!) {
  updatePost(id: $id, content: $content) {
    id
    version
    updatedAt
  }
}
```
