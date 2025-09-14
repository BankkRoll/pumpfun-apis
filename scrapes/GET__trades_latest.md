# GET /trades/latest

## Description
API endpoint for trade-related operations and data.

## Base URL
`https://frontend-api-v3.pump.fun`

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |

### Example Request
```bash
curl -X GET "https://frontend-api-v3.pump.fun/trades/latest" \
  -H "Authorization: Bearer YOUR_JWT_TOKEN"
```

## Response Examples

### Example 1
**Status:** `200`

**Response Data:**
```json
{
  "signature": "3t1ytFrj7oPrsMEdMyi1pH2i3Nckz1Hi57GsfkqdUokTmjfhg1SeCZYFxgdYGsuv1SEBLkifcoET1q6cdnAFmDWj",
  "mint": "DaCnDzf4wbPRYkJ774F7fp5hZdoFxXCATJ65h3xwpump",
  "sol_amount": 1007512915,
  "token_amount": 9057739107518,
  "is_buy": false,
  "user": "CRfU3Pe4Txsw8dMn78PehXmQCT7WGmtELPHUJWMG2RVB",
  "timestamp": 1757858642,
  "symbol": "TRDC",
  "image_uri": "https://ipfs.io/ipfs/QmW6hSzWMQLxM3iBAnNsxbt2h2Q67aRdrAjfzF28SAE9FY",
  "slot": 366780186
}
```

## Response Fields
| Field | Type | Description |
|-------|------|-------------|
| `status` | integer | HTTP status code |
| `data` | object | Response data (varies by endpoint) |

## Notes
- This endpoint provides real-time data from the Pump.fun API
- Response format may vary based on parameters and authentication
- All timestamps are in UNIX format unless otherwise specified
