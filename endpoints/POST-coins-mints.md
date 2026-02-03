# POST /coins/mints

## Endpoint Information

- **URL:** `https://advanced-api-v2.pump.fun/coins/mints`
- **Method:** `POST`
- **API:** `advanced-api-v2`
- **Operation ID:** `CoinsController_getCoinsByMints`

## Authentication

Requires JWT authentication via `Authorization: Bearer <token>` header.

## Parameters

*None*

## Request Body

**Content-Type:** `application/json`

```json
{
  "$ref": "#/components/schemas/GetMintsDto"
}
```

## Responses

### 201
## Example Usage

### cURL

```bash
curl -X POST "https://advanced-api-v2.pump.fun/coins/mints" \
  -H "Authorization: Bearer <your_token>" \
  -H "Accept: application/json" \
  -H "Content-Type: application/json" \
  -d '{"key": "value"}'
```

### Python

```python
import requests

url = "https://advanced-api-v2.pump.fun/coins/mints"
headers = {
    "Authorization": "Bearer <your_token>",
    "Accept": "application/json"
}

data = {"key": "value"}

response = requests.post(url, headers=headers, json=data)
print(response.json())
```

## Notes

- Replace `<your_token>` with your actual JWT token
- Replace path/query parameters with actual values
- Refer to the response schema for expected data structure