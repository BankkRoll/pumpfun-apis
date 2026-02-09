# PUT /livestreams/update-livestream

## Endpoint Information

- **URL:** `https://frontend-api-v3.pump.fun/livestreams/update-livestream`
- **Method:** `PUT`
- **API:** `frontend-api`
- **Operation ID:** `LivestreamController_updateLivestream`

## Authentication

Requires JWT authentication via `Authorization: Bearer <token>` header.

## Parameters

_None_

## Request Body

**Content-Type:** `application/json`

```json
{
  "$ref": "#/components/schemas/LivestreamDto"
}
```

## Responses

### 200

## Example Usage

### cURL

```bash
curl -X PUT "https://frontend-api-v3.pump.fun/livestreams/update-livestream" \
  -H "Authorization: Bearer <your_token>" \
  -H "Accept: application/json" \
  -H "Content-Type: application/json" \
  -d '{"key": "value"}'
```

### Python

```python
import requests

url = "https://frontend-api-v3.pump.fun/livestreams/update-livestream"
headers = {
    "Authorization": "Bearer <your_token>",
    "Accept": "application/json"
}

data = {"key": "value"}

response = requests.put(url, headers=headers, json=data)
print(response.json())
```

## Notes

- Replace `<your_token>` with your actual JWT token
- Replace path/query parameters with actual values
- Refer to the response schema for expected data structure
