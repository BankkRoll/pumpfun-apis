# POST /coins/mints

## Description
Fetch metadata for multiple coin mints at once.

## Base URL
`https://frontend-api-v3.pump.fun`

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Content-Type` | `application/json` | Yes |
| `Authorization` | `Bearer <JWT>` | Yes |

## Request Body
```json
{
  "mints": [
    "9LjLmk78kDbpsR18kYcdbEJe9yWALwkkSWaXA76Epump",
    "HQDTzNa4nQVetoG6aCbSLX9kcH7tSv2j2sTV67Etpump"
  ]
}
```

### Request Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `mints` | array | Yes | Array of mint addresses (strings) |

### Example Request
```bash
curl -X POST "https://frontend-api-v3.pump.fun/coins/mints" \
  -H "Authorization: Bearer YOUR_JWT_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
    "mints": [
      "9LjLmk78kDbpsR18kYcdbEJe9yWALwkkSWaXA76Epump",
      "HQDTzNa4nQVetoG6aCbSLX9kcH7tSv2j2sTV67Etpump"
    ]
  }'
```

## Response
**Status:** `201 Created`

```json
[
  {
    "mint": "9LjLmk78kDbpsR18kYcdbEJe9yWALwkkSWaXA76Epump",
    "name": "Clip Coin",
    "symbol": "CLIP",
    "description": "Simply tag us under your clip, with a wallet - and you will be PAID!",
    "image_uri": "https://ipfs.io/ipfs/bafkreihogclj4fu4llj242hcfrxueyxfvq7qgrolejnrnmo6uhudentfaa",
    "metadata_uri": "https://ipfs.io/ipfs/bafkreiegkcmuytjny2wjs43ygnni73lfnyysvmdbkxwgrsipeh3scseitu",
    "twitter": "https://x.com/i/communities/1966974261320384961",
    "telegram": null,
    "bonding_curve": "8wzhBE7rvNQVgHknPVeCGpFrWe9ZLycvLvb4tiTCAdTC",
    "associated_bonding_curve": "F3PZ81qhnugb7cyWKJC55uNWBVB9oM99mFrf9Se6LuPb",
    "creator": "22EYZ72LLvzDKzEgMWXURoSNwkxckeJRS3MKoNQA2u1a",
    "created_timestamp": 1757813746880,
    "raydium_pool": null,
    "complete": true,
    "virtual_sol_reserves": 109622849503,
    "virtual_token_reserves": 293643161322274,
    "total_supply": 1000000000000000,
    "website": null,
    "show_name": true,
    "king_of_the_hill_timestamp": 1757813943000,
    "market_cap": 11196.913677608723,
    "reply_count": 73,
    "last_reply": 1757854105000,
    "nsfw": false,
    "market_id": null,
    "banner_uri": null,
    "video_uri": null,
    "is_banned": false,
    "program": null,
    "usd_market_cap": 2753545.011597537,
    "is_currently_live": false
  }
]
```

## Response Fields
| Field | Type | Description |
|-------|------|-------------|
| `mint` | string | Mint address of the coin |
| `name` | string | Coin name |
| `symbol` | string | Coin symbol |
| `description` | string | Coin description |
| `image_uri` | string | URL to coin image |
| `metadata_uri` | string | URL to full metadata JSON |
| `twitter` | string | Twitter/X link |
| `telegram` | string | Telegram group link |
| `bonding_curve` | string | Primary bonding curve ID |
| `associated_bonding_curve` | string | Secondary bonding curve ID |
| `creator` | string | Creator wallet address |
| `created_timestamp` | integer | Unix timestamp of creation |
| `raydium_pool` | string/null | Associated Raydium liquidity pool |
| `complete` | boolean | Metadata completeness |
| `virtual_sol_reserves` | integer | Virtual SOL reserves |
| `virtual_token_reserves` | integer | Virtual token reserves |
| `total_supply` | integer | Total token supply |
| `website` | string | Website URL (nullable) |
| `show_name` | boolean | Whether to display name publicly |
| `king_of_the_hill_timestamp` | integer | Timestamp for KOTH events |
| `market_cap` | float | Market cap in native tokens |
| `reply_count` | integer | Number of replies/comments |
| `last_reply` | integer | Timestamp of last reply |
| `nsfw` | boolean | NSFW flag |
| `usd_market_cap` | float | Market cap in USD |
| `is_currently_live` | boolean | Whether live event is ongoing |
