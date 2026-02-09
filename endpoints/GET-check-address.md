# GET /check/{address}

## Endpoint Information

- **URL:** `https://frontend-api-v3.pump.fun/check/{address}`
- **Method:** `GET`
- **API:** `frontend-api`
- **Operation ID:** `WalletScreeningController_check`

## Authentication

Requires JWT authentication via `Authorization: Bearer <token>` header.

## Parameters

| Parameter | Type     | In   | Required | Description |
| --------- | -------- | ---- | -------- | ----------- |
| `address` | `string` | path | ✓        |             |

## Responses

### 200

## Example Usage

### cURL

```bash
curl -X GET "https://frontend-api-v3.pump.fun/check/<address>" \
  -H "Authorization: Bearer <your_token>" \
  -H "Accept: application/json"
```

### Python

```python
import requests

url = "https://frontend-api-v3.pump.fun/check/<address>"
headers = {
    "Authorization": "Bearer <your_token>",
    "Accept": "application/json"
}

response = requests.get(url, headers=headers)
print(response.json())
```

## Notes

- Replace `<your_token>` with your actual JWT token
- Replace path/query parameters with actual values
- Refer to the response schema for expected data structure
