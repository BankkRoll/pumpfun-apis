# GET /coins/featured

## Description
Fetch featured coins with advanced analytics and detailed holder information.

## Base URL
`https://advanced-api-v2.pump.fun`

## Query Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `keywordSearchActive` | boolean | No | Whether keyword search is active (default: false) |

### Example Request
```bash
curl -X GET "https://advanced-api-v2.pump.fun/coins/featured?keywordSearchActive=true" \
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
  "coins": [
    {
      "coinMint": "F3GV742i8n2p4t24hWAtvXeX6KCqhYArbKgvNAoZpump",
      "dev": "4dmgB5Zjt6fxCdq3t6nK2X1tWkpfwfDX3mRsE8vGU8PG",
      "name": "1$ Fees = 1 Tree planted",
      "ticker": "1$=1TREE",
      "imageUrl": "https://ipfs.io/ipfs/bafkreif5gdhngawyu5eqerb5vunczhw4x6f3asgdzp423c6nfwci2fz544",
      "creationTime": 1757854484064,
      "numHolders": 108,
      "marketCap": 10377.54,
      "volume": 732.183,
      "currentMarketPrice": 0,
      "bondingCurveProgress": 25.25,
      "sniperCount": 13,
      "graduationDate": null,
      "holders": [
        {
          "totalTokenAmountHeld": 22512623.547259,
          "isSniper": false,
          "ownedPercentage": 2.2512623547259,
          "holderId": "4bFxU3DJvVdqd7ETrAbPMzrJJHDmkPBsDu4yGhqZa9eH"
        }
      ],
      "allTimeHighMarketCap": 55567.42,
      "poolAddress": null,
      "twitter": "https://x.com/CryptoCurt31/status/1967210163686998109",
      "telegram": null,
      "website": "https://plantwithpurpose.org/plant-a-tree/",
      "hasTwitter": true,
      "hasTelegram": false,
      "hasWebsite": true,
      "hasSocial": true,
      "twitterReuseCount": 1,
      "devHoldingsPercentage": 0,
      "buyTransactions": 1270,
      "sellTransactions": 1062,
      "transactions": 2332,
      "sniperOwnedPercentage": 0,
      "topHoldersPercentage": 11.373621192945599
    }
  ]
}
```

## Response Fields
| Field | Type | Description |
|-------|------|-------------|
| `coins` | array | Array of featured coin objects with advanced analytics |

### Coin Object Fields
Same as GET /coins/list response fields.

## Notes
- Featured coins are curated selections with high engagement
- Includes detailed holder analytics and social presence indicators
- Provides comprehensive trading statistics and market data
