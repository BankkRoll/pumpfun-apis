# GET /bookmarks

## Description
API endpoint for managing user bookmarks.

## Base URL
`https://frontend-api-v3.pump.fun`

## Query Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `withPreviewImages` | boolean | Yes | No description available |

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |

### Example Request
```bash
curl -X GET "https://frontend-api-v3.pump.fun/bookmarks" \
  -H "Authorization: Bearer YOUR_JWT_TOKEN"
```

## Response Examples

### Example 1
**Status:** `200`

**Parameters:**
```json
{
  "withPreviewImages": true
}
```

**Response Data:**
```json
{
  "0": {
    "id": "c90b3e5e-adb5-4d62-b3b2-e11ff9bd1e6c",
    "user_id": "suqh5sHtr8HyJ7q8scBimULPkPpA557prMG47xCHQfK",
    "name": "default",
    "created_at": "2025-09-14T13:14:31.571031+00:00",
    "bookmark_items": [
      "7Pnqg1S6MYrL6AP1ZXcToTHfdBbTB77ze6Y33qBBpump"
    ],
    "preview_images": [
      "https://ipfs.io/ipfs/QmZ84u8K8RHJAcRVZftgiuDPDmhwNFNBT7h6CUcYbdnejU"
    ]
  }
}
```

**Test Summary:**
- Total test cases: 2
- Successful responses: 2
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
