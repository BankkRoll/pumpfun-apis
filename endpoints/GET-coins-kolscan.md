# GET /coins/kolscan

## Endpoint Information

- **URL:** `https://advanced-api-v2.pump.fun/coins/kolscan`
- **Method:** `GET`
- **API:** `advanced-api-v2`
- **Operation ID:** `CoinsController_getKolscanCoins`

## Authentication

Requires JWT authentication via `Authorization: Bearer <token>` header.

## Parameters

*None*

## Responses

### 200
## Example Usage

### cURL

```bash
curl -X GET "https://advanced-api-v2.pump.fun/coins/kolscan" \
  -H "Authorization: Bearer <your_token>" \
  -H "Accept: application/json"
```

### Python

```python
import requests

url = "https://advanced-api-v2.pump.fun/coins/kolscan"
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