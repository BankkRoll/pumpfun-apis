# DELETE /bookmarks/{bookmarkId}

## Description
API endpoint for managing user bookmarks.

## Base URL
`https://frontend-api-v3.pump.fun`

## Query Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `bookmarkId` | string | Yes | No description available |

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |

### Example Request
```bash
curl -X DELETE "https://frontend-api-v3.pump.fun/bookmarks/{bookmarkId}" \
  -H "Authorization: Bearer YOUR_JWT_TOKEN"
```

## Response Examples

### Example 1 - Successful Deletion
**Status:** `200`

**Parameters:**
```json
{
  "bookmarkId": "c90b3e5e-adb5-4d62-b3b2-e11ff9bd1e6c"
}
```

**Response Data:**
```json
{
  "success": true
}
```

### Example 2 - Invalid UUID Error
**Status:** `200`

**Parameters:**
```json
{
  "bookmarkId": "test"
}
```

**Response Data:**
```json
{
  "code": "22P02",
  "details": null,
  "hint": null,
  "message": "invalid input syntax for type uuid: \"test\""
}
```

**Test Summary:**
- Total test cases: 4
- Successful responses: 3
- Error responses: 1

## Response Fields
| Field | Type | Description |
|-------|------|-------------|
| `status` | integer | HTTP status code |
| `data` | object | Response data (varies by endpoint) |

## Notes
- This endpoint provides real-time data from the Pump.fun API
- Response format may vary based on parameters and authentication
- All timestamps are in UNIX format unless otherwise specified
