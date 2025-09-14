# GET /bookmarks/default

## Description
Fetch the default bookmarks for the authenticated user.

## Base URL
`https://frontend-api-v3.pump.fun`

## Query Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `withDetails` | boolean | No | Whether to include detailed information (default: false) |

### Example Request
```bash
curl -X GET "https://frontend-api-v3.pump.fun/bookmarks/default?withDetails=true" \
  -H "Authorization: Bearer YOUR_JWT_TOKEN"
```

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |

## Response
**Status:** `200 OK`

```json
{
    "id": "c20b1e5s-adb4-4d62-b3b2-e61ff9bd1e6c",
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
                "total_supply": 1000000000000000,
                "website": null,
                "show_name": true,
                "last_trade_timestamp": 1757556208000,
                "king_of_the_hill_timestamp": 1757551201000,
                "market_cap": 116879.18945924968,
                "nsfw": false,
                "market_id": null,
                "inverted": true,
                "real_sol_reserves": 85005359711,
                "real_token_reserves": 0,
                "livestream_ban_expiry": 0,
                "last_reply": 1757854980000,
                "reply_count": 3154,
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
                "usd_market_cap": 28654102.087829653
            }
        }
    ]
}
```

## Response Fields
| Field | Type | Description |
|-------|------|-------------|
| `id` | string | Unique bookmark collection ID |
| `user_id` | string | User's wallet address |
| `name` | string | Bookmark collection name |
| `created_at` | string | ISO timestamp when collection was created |
| `items` | array | Array of bookmarked items |

### Item Object Fields
| Field | Type | Description |
|-------|------|-------------|
| `item_id` | string | Bookmarked item ID (coin mint address) |
| `created_at` | string | ISO timestamp when item was bookmarked |
| `details` | object | Full coin details object |

### Coin Details Object Fields
| Field | Type | Description |
|-------|------|-------------|
| `mint` | string | Coin mint address |
| `name` | string | Coin display name |
| `symbol` | string | Coin ticker symbol |
| `description` | string | Coin description |
| `image_uri` | string | IPFS URL to coin image |
| `metadata_uri` | string | IPFS URL to full metadata JSON |
| `twitter` | string/null | Twitter/X link |
| `telegram` | string/null | Telegram group link |
| `bonding_curve` | string | Primary bonding curve ID |
| `associated_bonding_curve` | string | Secondary bonding curve ID |
| `creator` | string | Creator wallet address |
| `created_timestamp` | integer | UNIX timestamp of creation |
| `raydium_pool` | string/null | Associated Raydium liquidity pool |
| `complete` | boolean | Metadata completeness |
| `virtual_sol_reserves` | integer | Virtual SOL reserves |
| `virtual_token_reserves` | integer | Virtual token reserves |
| `total_supply` | integer | Total token supply |
| `website` | string/null | Website URL |
| `show_name` | boolean | Whether to display name publicly |
| `last_trade_timestamp` | integer | Last trade UNIX timestamp |
| `king_of_the_hill_timestamp` | integer | Timestamp for KOTH events |
| `market_cap` | float | Market cap in native tokens |
| `nsfw` | boolean | NSFW flag |
| `market_id` | string/null | Market ID |
| `inverted` | boolean | Trading curve direction |
| `real_sol_reserves` | integer | Actual SOL reserves |
| `real_token_reserves` | integer | Actual token reserves |
| `livestream_ban_expiry` | integer | Livestream ban expiry timestamp |
| `last_reply` | integer | Timestamp of last reply |
| `reply_count` | integer | Number of replies |
| `is_banned` | boolean | Whether coin is banned |
| `is_currently_live` | boolean | Whether live event is ongoing |
| `initialized` | boolean | Initialization status |
| `video_uri` | string/null | Video URL |
| `updated_at` | string/null | Last update timestamp |
| `pump_swap_pool` | string | Pump swap pool address |
| `ath_market_cap` | float | All-time high market cap |
| `ath_market_cap_timestamp` | integer | ATH market cap timestamp |
| `banner_uri` | string/null | Banner image URL |
| `hide_banner` | boolean | Whether to hide banner |
| `livestream_downrank_score` | integer | Livestream downrank score |
| `program` | string/null | Program association |
| `platform` | string/null | Platform association |
| `usd_market_cap` | float | Market cap in USD |

## Notes
- Returns the same structure as GET /bookmarks but for the default collection
- The `withDetails` parameter controls whether additional metadata is included
- When no default bookmarks exist, the `items` array will be empty
- Requires authentication to access user's default bookmarks
