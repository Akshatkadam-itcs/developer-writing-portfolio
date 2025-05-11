# 2. Authentication

This section describes how to authenticate requests to the ProWriterSite API using Bearer tokens.

The ProWriterSite API uses  **Bearer Token Authentication** to secure it's endpoints.

All API requests must include a valid access token to request a header. Without it, the server will thow a 401 Unauthorized error.

## Getting an Access Token

To access protected endpoints, you must first obtain an access token by registering your application or account in the ProwriterSite platform.

- Contact support at `support@prowritersite.dev` to request API credentials.
- Once registered, you'll receive an API key and secret.
- Use those credentials to obtain a token (authentication flow depends on the OAuth2.0 or custom system).

##  Example Request with Bearer Token

Use the `Authorization` header in your API calls as shown below:

```http
GET /writers HTTP/1.1
Host: api.prowritersites.dev
Authorization: Bearer YOUR_ACCESS_TOKEN
