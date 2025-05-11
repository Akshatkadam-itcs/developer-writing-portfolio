# 3. API Endpoints

In order to access and manage the writer portfolios, client requests, assignments, etc. the ProWriteSite API provides multiple endpoints. All of these endpoints provides barries endpoints.

## Writers

### GET /writers

**Description:** Retrieves a list of all registered writers.

```http
GET /writers HTTP/1.1
Host: api.prowritersites.dev
Authorization: Bearer YOUR_ACCESS_TOKEN

Response Example:

[
  {
    "id": "w123",
    "name": "Ava Taylor",
    "expertise": "Technical Writing",
    "rating": 4.8
  },
  ...
]

### GET/writers/{id}

**Description:** Retrieves details of a specific writer by ID.

GET /writers/w123 HTTP/1.1
Authorization: Bearer YOUR_ACCESS_TOKEN

### POST /clients/requests

**Description:** Submit a new writing request as a client.

POST /clients/requests HTTP/1.1
Content-Type: application/json
Authorization: Bearer YOUR_ACCESS_TOKEN

Request Body Example:

{
  "title": "API Documentation Project",
  "description": "Need detailed docs for an internal API",
  "budget": 200,
  "deadline": "2025-06-01"
}

### GET /assignments

**Description:** Fetch assignments assigned to an authenticated writer.

GET /assignments HTTP/1.1
Authorization: Bearer YOUR_ACCESS_TOKEN

Error Handling

All endpoints return appropriate HTTP status codes. Example:

| Code | Message      |
| ---- | ------------ |
| 200  | OK           |
| 201  | Created      |
| 400  | Bad Request  |
| 401  | Unauthorized |
| 404  | Not Found    |
| 500  | Server Error |
