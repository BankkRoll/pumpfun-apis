# GET /following/single/{followId}

## Description
Check if a specific user is following another user.

## Base URL
`https://frontend-api-v3.pump.fun`

## Path Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `followId` | string | Yes | ID of the follow relationship to check |

## Query Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `userId` | string | Yes | User's wallet address to check following status for |

### Example Request
```bash
curl -X GET "https://frontend-api-v3.pump.fun/following/single/suqh5sHtr8HyJ7q8scBimULPkPpA557prMG47xCHQfK?userId=suqh5sHtr8HyJ7q8scBimULPkPpA557prMG47xCHQfK" \
  -H "Authorization: Bearer YOUR_JWT_TOKEN" \
  -H "If-None-Match: W/\"9b-18SguHYkQaQP4BEIkVJHoXKfes4\""
```

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |
| `If-None-Match` | `W/"9b-18SguHYkQaQP4BEIkVJHoXKfes4"` | No |

## Response
**Status:** `304 Not Modified` (when using If-None-Match header)

```json
No content
```

## Response Fields
| Field | Type | Description |
|-------|------|-------------|
| Returns 304 Not Modified when content hasn't changed | | |

## Notes
- Uses ETag caching for efficient data transfer
- Returns 304 when the content hasn't changed since the last request
- Requires authentication to check following status
- Used to determine if a user is following another specific user
