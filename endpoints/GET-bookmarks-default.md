# GET /bookmarks/default

## Description
Fetch the default bookmarks for the authenticated user.

## Base URL
`https://frontend-api-v3.pump.fun`

## Query Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `withDetails` | boolean | No | Whether to include detailed information (default: false) |

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |

## Response
**Status:** `200 OK`

```json
[]
```

## Response Fields
| Field | Type | Description |
|-------|------|-------------|
| Response is an empty array when no default bookmarks exist | | |

## Notes
- Returns an empty array when the user has no default bookmarks
- The `withDetails` parameter controls whether additional metadata is included
