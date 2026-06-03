# API Authentication

The proposed API uses bearer token authentication for all `/api/*` endpoints.

## Approach

- Send an `Authorization` header that contains a bearer token with each request.
- Treat upload, admin, and metadata mutations as authenticated operations.
- Use short-lived access tokens and refresh them outside the API surface documented here.

## Authorization expectations

- **Read access**: authenticated users can browse galleries and photo metadata.
- **Write access**: upload, update, favorite, and delete operations should require an authenticated user with edit rights.
- **Admin access**: dashboard-oriented actions should be restricted to trusted maintainers or gallery owners.

## Client guidance

- Handle `401 Unauthorized` by redirecting to sign-in or refreshing the session.
- Do not persist tokens in source control or static configuration files.
- Prefer secure, HTTP-only session storage when the application moves beyond mock data.
