# GET /coins/currently-live

## Description
Fetch a list of all coins that are currently live on the platform.

## Base URL
`https://frontend-api-v3.pump.fun`

## Query Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `offset` | integer | No | Pagination offset (default: 0) |
| `limit` | integer | No | Maximum number of results (default: 1000) |
| `includeNsfw` | boolean | No | Whether to include NSFW coins (default: false) |
| `order` | string | No | Sorting order, `ASC` or `DESC` (default: DESC) |

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |

## Response
**Status:** `200 OK`

```json
[
  {
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
    "market_cap": 113113.17774523885,
    "nsfw": false,
    "market_id": null,
    "inverted": true,
    "real_sol_reserves": 85005359711,
    "real_token_reserves": 0,
    "livestream_ban_expiry": 0,
    "last_reply": 1757853812000,
    "reply_count": 3152,
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
    "thumbnail": "https://prod-livestream-thumbnails-841162682567.s3.us-east-1.amazonaws.com/535897/1757849536184.jpeg",
    "thumbnail_updated_at": 1757849536184,
    "num_participants": 358,
    "downrank_score": 0,
    "usd_market_cap": 27816792.671109136
  }
]
```

## Response Fields
| Field | Type | Description |
|-------|------|-------------|
| `mint` | string | Coin mint address |
| `name` | string | Coin display name |
| `symbol` | string | Coin ticker symbol |
| `description` | string | Coin description |
| `image_uri` | string | IPFS URL to coin image |
| `metadata_uri` | string | IPFS URL to full metadata JSON |
| `twitter` | string | Official Twitter/X link |
| `telegram` | string | Official Telegram link |
| `bonding_curve` | string | Coin bonding curve address |
| `associated_bonding_curve` | string | Secondary bonding curve address |
| `creator` | string | Coin creator public key |
| `created_timestamp` | integer | UNIX timestamp of coin creation |
| `complete` | boolean | Whether the coin setup is complete |
| `virtual_sol_reserves` | integer | Virtual SOL reserves for trading |
| `virtual_token_reserves` | integer | Virtual token reserves for trading |
| `total_supply` | integer | Maximum token supply |
| `website` | string | Coin project website URL |
| `show_name` | boolean | Whether to display coin name publicly |
| `last_trade_timestamp` | integer | Last trade UNIX timestamp |
| `market_cap` | number | Market cap in platform-native units |
| `nsfw` | boolean | Whether the coin is NSFW |
| `inverted` | boolean | Trading curve direction |
| `real_sol_reserves` | integer | Actual SOL reserves |
| `real_token_reserves` | integer | Actual token reserves |
| `is_currently_live` | boolean | Whether coin is live for trading |
| `initialized` | boolean | Initialization status |
| `thumbnail` | string | Thumbnail image URL |
| `num_participants` | integer | Number of active participants |
| `usd_market_cap` | number | Market cap in USD |
