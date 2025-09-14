# GET /coins/search

## Description
Search for coins based on a query term with filtering, sorting, and pagination.

## Base URL
`https://frontend-api-v3.pump.fun`

## Query Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `limit` | integer | No | Maximum number of results (default: 50) |
| `offset` | integer | No | Pagination offset (default: 0) |
| `includeNsfw` | boolean | No | Whether to include NSFW coins (default: false) |
| `order` | string | No | Sort order, `ASC` or `DESC` (default: `DESC`) |
| `sort` | string | No | Field to sort by, e.g., `market_cap`, `created_timestamp` (default: `market_cap`) |
| `searchTerm` | string | No | Text query to search for coins |
| `type` | string | No | Search type, e.g., `hybrid` (default: `hybrid`) |

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |

## Response
**Status:** `200 OK`

```json
[
  {
    "mint": "CBQxnbAbakVewBtZPDRQcQVLWZCfNcD5u6uJDDBJpump",
    "name": "AI Research Orchestrator",
    "symbol": "ARO",
    "description": "ARO is the first efficient AI Orchestrator - Router - Aggregator in the world. Dissecting your research request intelligently and routing each task to the best AI on the market.",
    "image_uri": "https://ipfs.io/ipfs/Qme9W7WndQgC3jyo2Ux8bMJNjR2DMNvzHxEJHpK2exBDFu",
    "metadata_uri": "https://ipfs.io/ipfs/QmbbnSPQFTMyPq4weaBqpZcfSxCqCFpBFGXCQsP61spFQT",
    "twitter": "https://x.com/ai_orchestrator",
    "telegram": "https://t.me/AIResearchOrchestratorgroup",
    "bonding_curve": "2RJVdFLTCiRxfCJakAqiLS7sDXz8svEdWbh5q7xHLzWC",
    "associated_bonding_curve": "AfXgfyMWPRYjoaWwknzmWwg4j1nkRfyonNrczBwv1PU8",
    "creator": "hc1msb9FeTqzUHr5zZcFFTM4iXx264XoUZeLN9w3WnJ",
    "created_timestamp": 1738852188874,
    "raydium_pool": "5dzj7kntbD6K7SdHfNhxdGucfPZQSTWXRBhPmih4xKEY",
    "complete": true,
    "virtual_sol_reserves": 115005359220,
    "virtual_token_reserves": 279900000000000,
    "total_supply": 1000000000000000,
    "website": "https://aiorchestrator.io",
    "show_name": true,
    "king_of_the_hill_timestamp": 1738859563000,
    "market_cap": 1623,
    "reply_count": 17,
    "last_reply": 1738968985000,
    "nsfw": false,
    "market_id": "EttQPtRcYkj6nPYd345qEbVjsqp7ipJmTJ9JrMLw15TS",
    "banner_uri": null,
    "video_uri": null,
    "is_banned": false,
    "program": null,
    "usd_market_cap": 399128.16,
    "is_currently_live": false,
    "rec_id": "e17ff6b7-f1ef-4580-a764-07715dbe91ea"
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
| `raydium_pool` | string | Optional Raydium pool address |
| `complete` | boolean | Whether coin setup is complete |
| `virtual_sol_reserves` | integer | Virtual SOL reserves for trading |
| `virtual_token_reserves` | integer | Virtual token reserves for trading |
| `total_supply` | integer | Maximum token supply |
| `website` | string | Coin official website |
| `show_name` | boolean | Whether to display coin name publicly |
| `king_of_the_hill_timestamp` | integer | Timestamp of coin's "king of the hill" event |
| `market_cap` | number | Market cap in platform-native units |
| `reply_count` | integer | Number of replies on the coin livestream |
| `last_reply` | integer | Timestamp of last reply |
| `nsfw` | boolean | Whether the coin is NSFW |
| `market_id` | string | Coin market ID |
| `banner_uri` | string | URL to coin banner image |
| `video_uri` | string | URL to coin video |
| `is_banned` | boolean | Whether coin is banned |
| `program` | string | Optional program association |
| `usd_market_cap` | number | Market cap in USD |
| `is_currently_live` | boolean | Whether coin is live |
| `rec_id` | string | Unique recommendation ID for this user |
