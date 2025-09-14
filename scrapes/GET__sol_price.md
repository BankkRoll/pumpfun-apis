# GET /sol-price

## Description
API endpoint for /sol-price operations.

## Base URL
`https://frontend-api-v3.pump.fun`

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |

### Example Request
```bash
curl -X GET "https://frontend-api-v3.pump.fun/sol-price" \
  -H "Authorization: Bearer YOUR_JWT_TOKEN"
```

## Response Examples

### Example 1
**Status:** `200`

**Response Data:**
```json
{
  "solPrice": 244.2
}
```

## Response Fields
| Field | Type | Description |
|-------|------|-------------|
| `status` | integer | HTTP status code |
| `data` | object | Response data (varies by endpoint) |

## Notes
- This endpoint provides real-time data from the Pump.fun API
- Response format may vary based on parameters and authentication
- All timestamps are in UNIX format unless otherwise specified
