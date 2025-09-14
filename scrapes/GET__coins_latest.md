# GET /coins/latest

## Description
API endpoint for coin-related operations.

## Base URL
`https://frontend-api-v3.pump.fun`

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |

### Example Request
```bash
curl -X GET "https://frontend-api-v3.pump.fun/coins/latest" \
  -H "Authorization: Bearer YOUR_JWT_TOKEN"
```

## Response Examples

### Example 1
**Status:** `200`

**Response Data:**
```json
{
  "mint": "FZAMPVLcXQsXbWYg6hEfZS7A61ob2ZPrfrcA7vK8UUwQ",
  "name": "TRDC",
  "symbol": "TRDC",
  "description": "This discovery will rewrite crypto history AI memecoin Launchpad",
  "image_uri": "https://ipfs.io/ipfs/QmfD4m3zdzWVm45eNFHJvGCzBUCYgZv23GEh8hnTT7Qukk",
  "metadata_uri": "https://ipfs.io/ipfs/QmTgpVW94HZbYfV2fxnxd3AUWo5YNJEH8m6YChA4YuUrAj",
  "twitter": "",
  "telegram": "",
  "bonding_curve": "6Ce68LC3GWrcJ23YTMW2DxkPrn5ANVWaTEF12TLvympu",
  "associated_bonding_curve": "8GuJB83WSXLy3ffUk3rmDTDedjBMPcWy2y1GVxjBLiME",
  "...": "... and 34 more properties"
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
