# GET /coins/for-you

## Description
Fetch a personalized list of coins recommended for the authenticated user.

## Base URL
`https://frontend-api-v3.pump.fun`

## Query Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `offset` | integer | No | Pagination offset (default: 0) |
| `limit` | integer | No | Maximum number of results (default: 100) |
| `includeNsfw` | boolean | No | Whether to include NSFW coins (default: false) |
| `forceControlGroup` | boolean | No | Forces assignment to control group for A/B testing (default: false) |

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |

## Response
**Status:** `200 OK`

```json
[
  {
    "mint": "DnT2zKKcBcCiCghKtmfKrvx8oTcxZWnQZi6q8XwGpump",
    "name": "PUMPOD",
    "symbol": "$PUMPOD",
    "description": "This is your crypto native podcast, pump dot pod. We aim to host guests, speak freely, and educate users on crypto via live streamed podcast shows.",
    "image_uri": "https://ipfs.io/ipfs/bafybeiezktm74qxvri2yv6zxkf7pio2cg3cbh7wvq4c5fmubpeczd7n2oy",
    "metadata_uri": "https://ipfs.io/ipfs/bafkreigizje7rahh5x36sgiimp47vdhmt5mwa3ljtb7ywn5bzo3zhv2vce",
    "twitter": "https://x.com/pumpdotpod?s=21&t=sfzhFxKTTqY7dPGFiTo5SQ",
    "telegram": null,
    "bonding_curve": "4hsv77jJdvjro8zp4eAoWgfVriPYD25FMLzQxbuXsW62",
    "associated_bonding_curve": "GLg8Z6nGzQjpUKkGuofFVejcRjhqoNdxA69wJeN2iTQ",
    "creator": "Et1qDDMU4kY1W1rj1zBaUUm9YkDhEUN2qb8gSJz2FTAg",
    "created_timestamp": 1757852844273,
    "raydium_pool": null,
    "complete": true,
    "virtual_sol_reserves": 111047507582,
    "virtual_token_reserves": 289875934399547,
    "total_supply": 1000000000000000,
    "website": null,
    "show_name": true,
    "king_of_the_hill_timestamp": 1757853799000,
    "market_cap": 957.3922075001179,
    "reply_count": 3,
    "last_reply": 1757854441000,
    "nsfw": false,
    "market_id": null,
    "banner_uri": "https://ipfs.io/ipfs/bafybeictfdj42yfhvxd5cfaxbfnbrkzmjkcaxyxmylxl724esbnph6emg4",
    "video_uri": null,
    "is_banned": false,
    "program": null,
    "usd_market_cap": 235441.891668429,
    "is_currently_live": false,
    "rec_id": "7c2be4fd-52cd-4fa2-acce-75dd9d53e913"
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
| `complete` | boolean | Whether coin setup is complete |
| `virtual_sol_reserves` | integer | Virtual SOL reserves for trading |
| `virtual_token_reserves` | integer | Virtual token reserves for trading |
| `total_supply` | integer | Maximum token supply |
| `show_name` | boolean | Whether to display coin name publicly |
| `king_of_the_hill_timestamp` | integer | Timestamp of coin's "king of the hill" event |
| `market_cap` | number | Market cap in platform-native units |
| `reply_count` | integer | Number of replies on the coin livestream |
| `last_reply` | integer | Timestamp of last reply |
| `nsfw` | boolean | Whether the coin is NSFW |
| `banner_uri` | string | URL to coin banner image |
| `video_uri` | string | URL to coin video |
| `is_banned` | boolean | Whether coin is banned |
| `usd_market_cap` | number | Market cap in USD |
| `is_currently_live` | boolean | Whether coin is live |
| `rec_id` | string | Unique recommendation ID for this user |
