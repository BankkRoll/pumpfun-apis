# GET /global-params/{timestamp}

## Description
API endpoint for /global-params/{timestamp} operations.

## Base URL
`https://frontend-api-v3.pump.fun`

## Query Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `timestamp` | number | Yes | No description available |

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |

### Example Request
```bash
curl -X GET "https://frontend-api-v3.pump.fun/global-params/{timestamp}" \
  -H "Authorization: Bearer YOUR_JWT_TOKEN"
```

## Response Examples

### Example 1
**Status:** `200`

**Parameters:**
```json
{
  "timestamp": 1757858650
}
```

**Response Data:**
```json
{
  "slot": 0,
  "signature": "not-available",
  "initial_virtual_token_reserves": 1043000000000000,
  "initial_virtual_sol_reserves": 30000000000,
  "initial_real_token_reserves": 831200000000000,
  "token_total_supply": 1000000000000000,
  "fee_basis_points": 100,
  "timestamp": 0
}
```

**Test Summary:**
- Total test cases: 4
- Successful responses: 4
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
