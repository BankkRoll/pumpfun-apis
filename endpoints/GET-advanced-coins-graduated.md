# GET /coins/graduated

## Description
Fetch coins that have graduated from the bonding curve to Raydium liquidity pools.

## Base URL
`https://advanced-api-v2.pump.fun`

## Query Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| No specific parameters | | | |

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
      "coinMint": "2EysVs7ewYqHJ61Q9guSgakqt5D4ThxPsARATcDFpump",
      "dev": "6VoK1vRc9aTvrM9vmw4oEFM5HCPuGRT1T7beaiHRBqNx",
      "name": "Trading Fish",
      "ticker": "FISH",
      "imageUrl": "https://ipfs.io/ipfs/bafybeies5unu3iyb2iv4cq2iwhpdheqaucfqedn5avqybhmj4qp5j4wsbm",
      "creationTime": 1757852654505,
      "numHolders": 356,
      "marketCap": 89581.6181562,
      "volume": 985.5318,
      "currentMarketPrice": 0,
      "bondingCurveProgress": 100,
      "sniperCount": 3,
      "graduationDate": 1757854885369,
      "holders": [
        {
          "totalTokenAmountHeld": 130701835.680715,
          "isSniper": true,
          "ownedPercentage": 13.0701835680715,
          "holderId": "6VoK1vRc9aTvrM9vmw4oEFM5HCPuGRT1T7beaiHRBqNx"
        }
      ],
      "allTimeHighMarketCap": 126130.98939,
      "poolAddress": "G1z5KA61M58b7Dq4v5NVod41jkibEM5JSe4k5uLrL1SN",
      "twitter": null,
      "telegram": null,
      "website": null,
      "hasTwitter": false,
      "hasTelegram": false,
      "hasWebsite": false,
      "hasSocial": false,
      "twitterReuseCount": 0,
      "devHoldingsPercentage": 13.0701835681,
      "buyTransactions": 1230,
      "sellTransactions": 783,
      "transactions": 2013,
      "sniperOwnedPercentage": 0.130701835681,
      "topHoldersPercentage": 31.254576837
    },
    {
      "coinMint": "DnT2zKKcBcCiCghKtmfKrvx8oTcxZWnQZi6q8XwGpump",
      "dev": "Et1qDDMU4kY1W1rj1zBaUUm9YkDhEUN2qb8gSJz2FTAg",
      "name": "PUMPOD",
      "ticker": "$PUMPOD",
      "imageUrl": "https://ipfs.io/ipfs/bafybeiezktm74qxvri2yv6zxkf7pio2cg3cbh7wvq4c5fmubpeczd7n2oy",
      "creationTime": 1757852843769,
      "numHolders": 244,
      "marketCap": 189933.812971,
      "volume": 1367.5047,
      "currentMarketPrice": 0,
      "bondingCurveProgress": 100,
      "sniperCount": 2,
      "graduationDate": 1757853978192,
      "holders": [
        {
          "totalTokenAmountHeld": 303858407.06399,
          "isSniper": true,
          "ownedPercentage": 30.385840706398998,
          "holderId": "Et1qDDMU4kY1W1rj1zBaUUm9YkDhEUN2qb8gSJz2FTAg"
        }
      ],
      "allTimeHighMarketCap": 389392.00246,
      "poolAddress": "9e7TMoiwWGPxWXhyegbV1RTyLYrwMCaMho1qNjD2K2Pf",
      "twitter": "https://x.com/pumpdotpod?s=21&t=sfzhFxKTTqY7dPGFiTo5SQ",
      "telegram": null,
      "website": null,
      "hasTwitter": true,
      "hasTelegram": false,
      "hasWebsite": false,
      "hasSocial": true,
      "twitterReuseCount": 1,
      "devHoldingsPercentage": 30.3858407064,
      "buyTransactions": 1062,
      "sellTransactions": 1027,
      "transactions": 2089,
      "sniperOwnedPercentage": 0.303858407064,
      "topHoldersPercentage": 62.78057792949999
    }
  ]
}
```

## Response Fields
| Field | Type | Description |
|-------|------|-------------|
| `coins` | array | Array of graduated coin objects with advanced analytics |

### Coin Object Fields
Same as GET /coins/list response fields, with additional notes:

- `bondingCurveProgress` will always be 100 for graduated coins
- `graduationDate` contains the UNIX timestamp when the coin graduated
- `poolAddress` contains the Raydium liquidity pool address
- These coins have completed the bonding curve and are now trading on Raydium

## Notes
- Graduated coins have completed the bonding curve (100% progress)
- All graduated coins have associated Raydium pool addresses
- These coins are no longer trading on the pump.fun bonding curve
