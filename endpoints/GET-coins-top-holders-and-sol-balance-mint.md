# GET /coins/top-holders-and-sol-balance/{mint}

## Endpoint Information

- **URL:** `https://advanced-api-v2.pump.fun/coins/top-holders-and-sol-balance/{mint}`
- **Method:** `GET`
- **API:** `advanced-api-v2`
- **Operation ID:** `CoinsController_getTopHoldersAndSolBalance`

## Authentication

Requires JWT authentication via `Authorization: Bearer <token>` header.

## Parameters

| Parameter | Type | In | Required | Description |
|-----------|------|-----|----------|-------------|
| `mint` | `string` | path | ✓ |  |

## Responses

### 200
## Example Usage

### cURL

```bash
curl -X GET "https://advanced-api-v2.pump.fun/coins/top-holders-and-sol-balance/<mint>" \
  -H "Authorization: Bearer <your_token>" \
  -H "Accept: application/json"
```

### Python

```python
import requests

url = "https://advanced-api-v2.pump.fun/coins/top-holders-and-sol-balance/<mint>"
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