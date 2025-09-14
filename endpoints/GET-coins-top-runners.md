# GET /coins/top-runners

## Description
Fetch a curated list of coins currently performing the best on the platform.

## Base URL
`https://frontend-api-v3.pump.fun`

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |

## Response
**Status:** `200 OK`

```json
[
  {
    "coin": {
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
      "market_cap": 10866.56526209558,
      "reply_count": 73,
      "last_reply": 1757854105000,
      "nsfw": false,
      "market_id": null,
      "banner_uri": null,
      "video_uri": null,
      "is_banned": false,
      "program": null,
      "usd_market_cap": 2672305.729254545,
      "is_currently_live": false
    },
    "description": "Clip Coin Launches With Rewarding Payout Model for Clippers",
    "modifiedBy": "FmoMPpn9LjpY8MiigHhFZgm79RE1ynj2tsipz3a96icb"
  }
]
```

## Response Fields
| Field | Type | Description |
|-------|------|-------------|
| `coin` | object | Coin metadata object |
| `description` | string | Short news/summary about the coin |
| `modifiedBy` | string | ID of user who last modified the entry |

### Coin Object Fields
Same as POST /coins/mints response fields.
