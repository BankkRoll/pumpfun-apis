# GET /v1/pools/{poolId}/market-activity

## Description
API endpoint for retrieving market activity statistics for a specific trading pool over different time periods.

## Base URL
`https://swap-api.pump.fun`

## Path Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `poolId` | string | Yes | The unique identifier for the trading pool |

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |

### Example Request
```bash
curl -X GET "https://swap-api.pump.fun/v1/pools/{poolId}/market-activity" \
  -H "Authorization: Bearer YOUR_JWT_TOKEN"
```

## Response Examples

### Example 1 - Successful Response
**Status:** `200`

**Parameters:**
```json
{
  "poolId": "FBZSQpAYGQJpmRT8L33QnGwv6bCaTx6XCjmTPVCw3gdZ"
}
```

**Response Data:**
```json
{
  "5m": {
    "numTxs": 109,
    "volumeUSD": 25101.777832524094,
    "numUsers": 81,
    "numBuys": 43,
    "numSells": 66,
    "buyVolumeUSD": 15373.244396868055,
    "sellVolumeUSD": 9728.53343565604,
    "numBuyers": 32,
    "numSellers": 53,
    "priceChangePercent": 2.646029612296351
  },
  "1h": {
    "numTxs": 2553,
    "volumeUSD": 1126347.4822734625,
    "numUsers": 943,
    "numBuys": 1333,
    "numSells": 1220,
    "buyVolumeUSD": 573282.2007778239,
    "sellVolumeUSD": 553065.2814956385,
    "numBuyers": 550,
    "numSellers": 561,
    "priceChangePercent": 7.26701495824054
  },
  "6h": {
    "numTxs": 17647,
    "volumeUSD": 8020035.2901769355,
    "numUsers": 3786,
    "numBuys": 9166,
    "numSells": 8481,
    "buyVolumeUSD": 4022763.6775804036,
    "sellVolumeUSD": 3997271.612596532,
    "numBuyers": 2354,
    "numSellers": 2435,
    "priceChangePercent": 2.5667467481507003
  },
  "24h": {
    "numTxs": 128476,
    "volumeUSD": 52283867.24364046,
    "numUsers": 15319,
    "numBuys": 67601,
    "numSells": 60875,
    "buyVolumeUSD": 26345373.594966907,
    "sellVolumeUSD": 25938493.648673553,
    "numBuyers": 12666,
    "numSellers": 9618,
    "priceChangePercent": 520.5001705860045
  }
}
```

**Test Summary:**
- Total test cases: 1
- Successful responses: 1
- Error responses: 0

## Response Fields
| Field | Type | Description |
|-------|------|-------------|
| `5m` | object | Market activity data for the last 5 minutes |
| `1h` | object | Market activity data for the last 1 hour |
| `6h` | object | Market activity data for the last 6 hours |
| `24h` | object | Market activity data for the last 24 hours |

### Time Period Object Fields
| Field | Type | Description |
|-------|------|-------------|
| `numTxs` | integer | Total number of transactions |
| `volumeUSD` | number | Total trading volume in USD |
| `numUsers` | integer | Number of unique users who traded |
| `numBuys` | integer | Number of buy transactions |
| `numSells` | integer | Number of sell transactions |
| `buyVolumeUSD` | number | Total buy volume in USD |
| `sellVolumeUSD` | number | Total sell volume in USD |
| `numBuyers` | integer | Number of unique buyers |
| `numSellers` | integer | Number of unique sellers |
| `priceChangePercent` | number | Price change percentage for the time period |

## Notes
- This endpoint provides real-time market activity data from the Pump.fun Swap API
- Data is aggregated over different time periods (5m, 1h, 6h, 24h)
- All volume amounts are in USD
- Price change percentages are calculated relative to the start of each time period
- The poolId is typically a Solana public key (base58 encoded)
- Response includes both buy and sell activity breakdowns
