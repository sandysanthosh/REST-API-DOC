# REST API Error Response Standard

A predictable error response helps API consumers handle failures safely and makes production troubleshooting faster.

## Recommended JSON shape

```json
{
  "timestamp": "2026-09-19T16:00:00Z",
  "status": 400,
  "error": "VALIDATION_ERROR",
  "message": "One or more fields are invalid.",
  "path": "/api/v1/customers",
  "traceId": "3e4b0f5d1c"
}
```

For validation errors, include field-level details without exposing implementation internals:

```json
{
  "error": "VALIDATION_ERROR",
  "message": "One or more fields are invalid.",
  "fieldErrors": [
    { "field": "email", "message": "must be a valid email address" }
  ]
}
```

## HTTP status guidance

| Status | Use it when |
| --- | --- |
| 400 Bad Request | The request is malformed or fails validation. |
| 401 Unauthorized | Authentication is missing or invalid. |
| 403 Forbidden | The authenticated caller lacks permission. |
| 404 Not Found | The requested resource does not exist. |
| 409 Conflict | The request conflicts with current resource state, such as a duplicate unique key. |
| 422 Unprocessable Content | The request syntax is valid but cannot be processed because of business rules. |
| 429 Too Many Requests | The caller has exceeded a rate limit. |
| 500 Internal Server Error | An unexpected server failure occurred. |
| 503 Service Unavailable | A temporary dependency or service outage prevents processing. |

## Spring Boot implementation notes

- Use `@RestControllerAdvice` to centralize exception-to-response mapping.
- Return safe client messages; log the internal exception and stack trace on the server.
- Include a correlation or trace ID in both the response and logs.
- Never return secrets, SQL statements, stack traces, or internal hostnames to API consumers.
- Document errors in OpenAPI/Swagger alongside successful responses.
