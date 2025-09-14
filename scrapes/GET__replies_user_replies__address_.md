# GET /replies/user-replies/{address}

## Description
API endpoint for /replies/user-replies/{address} operations.

## Base URL
`https://frontend-api-v3.pump.fun`

## Query Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `address` | string | Yes | No description available |
| `limit` | number | Yes | No description available |
| `offset` | number | Yes | No description available |

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |

### Example Request
```bash
curl -X GET "https://frontend-api-v3.pump.fun/replies/user-replies/{address}" \
  -H "Authorization: Bearer YOUR_JWT_TOKEN"
```

## Response Examples

### Example 1
**Status:** `200`

**Parameters:**
```json
{
  "limit": 10,
  "offset": 0
}
```

**Response Data:**
```json
{
  "replies": [],
  "hasMore": false,
  "offset": 0
}
```

**Test Summary:**
- Total test cases: 5
- Successful responses: 5
- Error responses: 0

## Response Fields
| Field | Type | Description |
|-------|------|-------------|
| `status` | integer | HTTP status code |
| `data` | object | Response data (varies by endpoint) |

## Notes
- This endpoint provides real-time data from the Pump.fun API
- Response format may vary based on parameters and authentication
- All timestamps are in UNIX format unless otherwise specified
