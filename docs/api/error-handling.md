# API Error Handling

Use a consistent JSON error envelope across all endpoints.

## Error shape

```json
{
  "error": "BadRequest",
  "message": "The request payload is invalid.",
  "statusCode": 400,
  "requestId": "req_01hxyz123abc"
}
```

## Guidelines

- Keep `message` actionable and safe to expose to clients.
- Use `requestId` to correlate client reports with server logs.
- Reserve `5xx` errors for unexpected failures; use `4xx` codes for validation, auth, or not-found cases.

## Recommended status codes

- `400` — invalid query params, invalid payloads, unsupported files.
- `401` — missing or invalid authentication.
- `404` — photo, upload, or tag resource not found.
- `413` — upload too large.
- `500` — unexpected server-side failure.

## Frontend handling

- Display inline validation feedback for `400` responses.
- Prompt for re-authentication on `401` responses.
- Show a retry-friendly message for `500` responses.
- Preserve user-selected filters and form state when requests fail.
