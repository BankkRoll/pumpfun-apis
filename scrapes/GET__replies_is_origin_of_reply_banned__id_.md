# GET /replies/is-origin-of-reply-banned/{id}

## Description
API endpoint for /replies/is-origin-of-reply-banned/{id} operations.

## Base URL
`https://frontend-api-v3.pump.fun`

## Query Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `id` | number | Yes | No description available |

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |

### Example Request
```bash
curl -X GET "https://frontend-api-v3.pump.fun/replies/is-origin-of-reply-banned/{id}" \
  -H "Authorization: Bearer YOUR_JWT_TOKEN"
```

## Response Examples

### Example 1
**Status:** `200`

**Parameters:**
```json
{
  "id": ""
}
```

**Test Summary:**
- Total test cases: 5
- Successful responses: 1
- Error responses: 4

## Response Fields
| Field | Type | Description |
|-------|------|-------------|
| `status` | integer | HTTP status code |
| `data` | object | Response data (varies by endpoint) |

## Notes
- This endpoint provides real-time data from the Pump.fun API
- Response format may vary based on parameters and authentication
- All timestamps are in UNIX format unless otherwise specified
