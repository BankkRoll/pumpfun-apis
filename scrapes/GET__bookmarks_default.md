# GET /bookmarks/default

## Description
API endpoint for managing user bookmarks.

## Base URL
`https://frontend-api-v3.pump.fun`

## Query Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `withDetails` | boolean | Yes | No description available |

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |

### Example Request
```bash
curl -X GET "https://frontend-api-v3.pump.fun/bookmarks/default" \
  -H "Authorization: Bearer YOUR_JWT_TOKEN"
```

## Response Examples

### Example 1
**Status:** `200`

**Parameters:**
```json
{
  "withDetails": true
}
```

**Response Data:**
```json
{
  "id": "c90b3e5e-adb5-4d62-b3b2-e11ff9bd1e6c",
  "user_id": "suqh5sHtr8HyJ7q8scBimULPkPpA557prMG47xCHQfK",
  "name": "default",
  "created_at": "2025-09-14T13:14:31.571031+00:00",
  "items": [
    {
      "item_id": "7Pnqg1S6MYrL6AP1ZXcToTHfdBbTB77ze6Y33qBBpump",
      "created_at": "2025-09-14T13:14:31.635853+00:00",
      "details": {
        "mint": "7Pnqg1S6MYrL6AP1ZXcToTHfdBbTB77ze6Y33qBBpump",
        "name": "Bagwork",
        "symbol": "Bagwork",
        "description": "",
        "image_uri": "https://ipfs.io/ipfs/QmZ84u8K8RHJAcRVZftgiuDPDmhwNFNBT7h6CUcYbdnejU",
        "metadata_uri": "https://ipfs.io/ipfs/QmYcDy5CaWErU81pQ9hfZt5wsDxYpdRBYhggvUTPFk135N",
        "twitter": "https://x.com/i/communities/1965925295229460830",
        "telegram": null,
        "bonding_curve": "27kydcn8k35y28EUM52NQaagAz3tJm6v3ZZoAY9fhxSv",
        "associated_bonding_curve": "6fUELiLxRm5FHvrCd3LjLanFBwTVa8STjz29B57uGX2k",
        "creator": "BcPrjBd7NNQyh5xoEdYWjVXDRwwejMHXMhPCWCYyjReR",
        "created_timestamp": 1757550077786,
        "raydium_pool": null,
        "complete": true,
        "virtual_sol_reserves": 115005359711,
        "virtual_token_reserves": 279900000000000,
        "hidden": null,
        "total_supply": 1000000000000000,
        "website": null,
        "show_name": true,
        "last_trade_timestamp": 1757556208000,
        "king_of_the_hill_timestamp": 1757551201000,
        "market_cap": 112492.37493923298,
        "nsfw": false,
        "market_id": null,
        "inverted": true,
        "real_sol_reserves": 85005359711,
        "real_token_reserves": 0,
        "livestream_ban_expiry": 0,
        "last_reply": 1757858081000,
        "reply_count": 3156,
        "is_banned": false,
        "is_currently_live": true,
        "initialized": true,
        "video_uri": null,
        "updated_at": null,
        "pump_swap_pool": "FBZSQpAYGQJpmRT8L33QnGwv6bCaTx6XCjmTPVCw3gdZ",
        "ath_market_cap": 35463423.16528456,
        "ath_market_cap_timestamp": 1757807154005,
        "banner_uri": null,
        "hide_banner": false,
        "livestream_downrank_score": 0,
        "program": null,
        "platform": null,
        "usd_market_cap": 27465013.341413733
      }
    }
  ]
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
