# GET /following/{address}

## Description
Fetch all users that a specific user is following.

## Base URL
`https://frontend-api-v3.pump.fun`

## Path Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `address` | string | Yes | User's wallet address |

### Example Request
```bash
curl -X GET "https://frontend-api-v3.pump.fun/following/suqh5sHtr8HyJ7q8scBimULPkPpA557prMG47xCHQfK" \
  -H "Authorization: Bearer YOUR_JWT_TOKEN" \
  -H "If-None-Match: W/\"2-l9Fw4VUO7kr8CvBlt4zaMCqXZ0w\""
```

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |
| `If-None-Match` | `W/"2-l9Fw4VUO7kr8CvBlt4zaMCqXZ0w"` | No |

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
- Requires authentication to access following list
