# GET /coins/volatile

## Description
Fetch coins with the highest volatility scores, indicating the most volatile trading activity.

## Base URL
`https://volatility-api-v2.pump.fun`

## Query Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `nsfw` | boolean | No | Whether to include NSFW coins (default: false) |
| `limit` | integer | No | Maximum number of results (default: 20) |
| `offset` | integer | No | Pagination offset (default: 0) |
| `worker` | string | No | Worker identifier (default: DEFAULT) |

### Example Request
```bash
curl -X GET "https://volatility-api-v2.pump.fun/coins/volatile?limit=10&offset=0&nsfw=false&worker=DEFAULT" \
  -H "If-None-Match: W/\"2d16-1svuY47pO5vx7mjD+Loc2K2xnYM\""
```

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `If-None-Match` | `W/"2d16-1svuY47pO5vx7mjD+Loc2K2xnYM"` | No |

## Response
**Status:** `200 OK`

```json
[
  {
    "mint": "F3GV742i8n2p4t24hWAtvXeX6KCqhYArbKgvNAoZpump",
    "name": "1$ Fees = 1 Tree planted",
    "symbol": "1$=1TREE",
    "description": "",
    "created_at": 1757854484247,
    "volatility_score": 166.51226838353688,
    "usd_market_cap": 18960.436978308982,
    "image_uri": "https://ipfs.io/ipfs/bafkreif5gdhngawyu5eqerb5vunczhw4x6f3asgdzp423c6nfwci2fz544",
    "video_uri": null,
    "metadata_uri": "https://ipfs.io/ipfs/bafkreicfu73ej23brfnj6mmzhb5ik7bvwfatevcwn5cctzxnhpiboyzw3m",
    "nsfw": false,
    "usd_ath_market_cap": 53512.020206770045,
    "updated_at": "2025-09-14T13:01:53.727Z"
  },
  {
    "mint": "9RQK5RqXSAu4DJ1Ajp56gMwK2x8kG8x8DcseEUWnpump",
    "name": "MR FEED",
    "symbol": "MR FEED",
    "description": "we feed poor and hungry people those who are really in need we donate food supplies as well ",
    "created_at": 1757854581538,
    "volatility_score": 156.80995623560653,
    "usd_market_cap": 33211.48227198172,
    "image_uri": "https://ipfs.io/ipfs/QmXUt7a7eVBFKscyTTrjqJtV9WRR3UMTLMugoLJ1PZ71oP",
    "video_uri": null,
    "metadata_uri": "https://ipfs.io/ipfs/QmRCMAZJp44z6hrZbnoYvespzCzTUPTycc7rbajXuDos1H",
    "nsfw": false,
    "usd_ath_market_cap": 60895.45733581166,
    "updated_at": "2025-09-14T13:01:53.730Z"
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
| `created_at` | integer | UNIX timestamp of coin creation |
| `volatility_score` | float | Volatility score (higher = more volatile) |
| `usd_market_cap` | float | Current market cap in USD |
| `image_uri` | string | IPFS URL to coin image |
| `video_uri` | string/null | URL to coin video |
| `metadata_uri` | string | IPFS URL to full metadata JSON |
| `nsfw` | boolean | Whether the coin is NSFW |
| `usd_ath_market_cap` | float | All-time high market cap in USD |
| `updated_at` | string | ISO timestamp of last update |
