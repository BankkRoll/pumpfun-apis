# GET /coins/user-created-coins/{address}

## Description
Fetch all coins created by a specific user.

## Base URL
`https://frontend-api-v3.pump.fun`

## Path Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `address` | string | Yes | User's wallet address |

## Query Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `offset` | integer | No | Pagination offset (default: 0) |
| `limit` | integer | No | Maximum number of results (default: 50) |
| `includeNsfw` | boolean | No | Whether to include NSFW coins (default: false) |

### Example Request
```bash
curl -X GET "https://frontend-api-v3.pump.fun/coins/user-created-coins/suqh5sHtr8HyJ7q8scBimULPkPpA557prMG47xCHQfK?offset=0&limit=10" \
  -H "Authorization: Bearer YOUR_JWT_TOKEN" \
  -H "If-None-Match: W/\"16-5DZZ+gejm6YGnrGTvOOY/LJbWyU\""
```

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |
| `If-None-Match` | `W/"16-5DZZ+gejm6YGnrGTvOOY/LJbWyU"` | No |

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
- Requires authentication to access user's created coins
- Supports pagination with offset and limit parameters
