# GET /coins/list

## Description
Fetch a list of coins with advanced analytics and detailed holder information.

## Base URL
`https://advanced-api-v2.pump.fun`

## Query Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `sortBy` | string | No | Field to sort by (e.g., `creationTime`) |
| `direction` | string | No | Sort direction (`asc` or `desc`) |

### Example Request
```bash
curl -X GET "https://advanced-api-v2.pump.fun/coins/list?sortBy=creationTime&direction=desc" \
  -H "Authorization: Bearer YOUR_JWT_TOKEN" \
  -H "If-None-Match: W/\"a89a-6nmClpVshjL1gjKboGl7RQ3YVKM\""
```

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |
| `If-None-Match` | `W/"a89a-6nmClpVshjL1gjKboGl7RQ3YVKM"` | No |

## Response
**Status:** `200 OK`

```json
{
  "coins": [
    {
      "coinMint": "5Ykt5Mp9jZUg27MiRoiKhfW24e4n7B1zjQQKQKRkpump",
      "dev": "EAvYekEuVrbagnfog5KYtMejhyj4AABxf5awcGkhRnhS",
      "name": "The Creator Economy",
      "ticker": "TCE",
      "imageUrl": "https://ipfs.io/ipfs/bafkreicemvwdxmktevo6hanhwbnbv6z62umwjafrr2uxjufxnmpznngsxe",
      "creationTime": 1757855042115,
      "numHolders": 8,
      "marketCap": 9823.48,
      "volume": 7.0098,
      "currentMarketPrice": 0,
      "bondingCurveProgress": 22.26,
      "sniperCount": 8,
      "graduationDate": null,
      "holders": [
        {
          "totalTokenAmountHeld": 151660777.360416,
          "isSniper": true,
          "ownedPercentage": 15.166077736041599,
          "holderId": "EAvYekEuVrbagnfog5KYtMejhyj4AABxf5awcGkhRnhS"
        }
      ],
      "allTimeHighMarketCap": 10127.39,
      "poolAddress": null,
      "twitter": "https://x.com/a1lon9/status/1967210705364660608",
      "telegram": null,
      "website": null,
      "hasTwitter": true,
      "hasTelegram": false,
      "hasWebsite": false,
      "hasSocial": true,
      "twitterReuseCount": 1,
      "devHoldingsPercentage": 15.166077736000002,
      "buyTransactions": 8,
      "sellTransactions": 1,
      "transactions": 9,
      "sniperOwnedPercentage": 0.176525162184,
      "topHoldersPercentage": 17.6525162184
    }
  ]
}
```

## Response Fields
| Field | Type | Description |
|-------|------|-------------|
| `coins` | array | Array of coin objects with advanced analytics |

### Coin Object Fields
| Field | Type | Description |
|-------|------|-------------|
| `coinMint` | string | Coin mint address |
| `dev` | string | Developer/creator wallet address |
| `name` | string | Coin display name |
| `ticker` | string | Coin ticker symbol |
| `imageUrl` | string | URL to coin image |
| `creationTime` | integer | UNIX timestamp of creation |
| `numHolders` | integer | Number of token holders |
| `marketCap` | float | Current market cap |
| `volume` | float | Trading volume |
| `currentMarketPrice` | float | Current market price |
| `bondingCurveProgress` | float | Bonding curve completion percentage |
| `sniperCount` | integer | Number of sniper addresses |
| `graduationDate` | integer/null | UNIX timestamp of graduation to Raydium |
| `holders` | array | Array of holder objects |
| `allTimeHighMarketCap` | float | All-time high market cap |
| `poolAddress` | string/null | Raydium pool address |
| `twitter` | string/null | Twitter URL |
| `telegram` | string/null | Telegram URL |
| `website` | string/null | Website URL |
| `hasTwitter` | boolean | Has Twitter presence |
| `hasTelegram` | boolean | Has Telegram presence |
| `hasWebsite` | boolean | Has website |
| `hasSocial` | boolean | Has any social presence |
| `twitterReuseCount` | integer | Number of times Twitter URL reused |
| `devHoldingsPercentage` | float | Developer's token holdings percentage |
| `buyTransactions` | integer | Number of buy transactions |
| `sellTransactions` | integer | Number of sell transactions |
| `transactions` | integer | Total transactions |
| `sniperOwnedPercentage` | float | Percentage owned by snipers |
| `topHoldersPercentage` | float | Percentage owned by top holders |

### Holder Object Fields
| Field | Type | Description |
|-------|------|-------------|
| `totalTokenAmountHeld` | float | Total tokens held |
| `isSniper` | boolean | Whether this is a sniper address |
| `ownedPercentage` | float | Percentage of total supply owned |
| `holderId` | string | Holder's wallet address |
