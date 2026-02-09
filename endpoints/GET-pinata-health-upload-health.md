# GET /pinata-health/upload-health

## Endpoint Information

- **URL:** `https://frontend-api-v3.pump.fun/pinata-health/upload-health`
- **Method:** `GET`
- **API:** `frontend-api`
- **Operation ID:** `PinataHealthController_getUploadHealth`

## Authentication

Requires JWT authentication via `Authorization: Bearer <token>` header.

## Parameters

_None_

## Responses

### 200

## Example Usage

### cURL

```bash
curl -X GET "https://frontend-api-v3.pump.fun/pinata-health/upload-health" \
  -H "Authorization: Bearer <your_token>" \
  -H "Accept: application/json"
```

### Python

```python
import requests

url = "https://frontend-api-v3.pump.fun/pinata-health/upload-health"
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
