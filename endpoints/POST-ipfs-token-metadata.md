# POST /ipfs/token-metadata

## Endpoint Information

- **URL:** `https://frontend-api-v3.pump.fun/ipfs/token-metadata`
- **Method:** `POST`
- **API:** `frontend-api`
- **Operation ID:** `IpfsController_uploadFile`

## Authentication

Requires JWT authentication via `Authorization: Bearer <token>` header.

## Parameters

_None_

## Request Body

**Content-Type:** `application/json`

```json
{
  "$ref": "#/components/schemas/UploadMetadataDto"
}
```

## Responses

### 201

## Example Usage

### cURL

```bash
curl -X POST "https://frontend-api-v3.pump.fun/ipfs/token-metadata" \
  -H "Authorization: Bearer <your_token>" \
  -H "Accept: application/json" \
  -H "Content-Type: application/json" \
  -d '{"key": "value"}'
```

### Python

```python
import requests

url = "https://frontend-api-v3.pump.fun/ipfs/token-metadata"
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
