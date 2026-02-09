# GET /livestreams/stream/livestream-token

## Endpoint Information

- **URL:** `https://frontend-api-v3.pump.fun/livestreams/stream/livestream-token`
- **Method:** `GET`
- **API:** `frontend-api`
- **Operation ID:** `LivestreamController_getStreamToken`

## Authentication

Requires JWT authentication via `Authorization: Bearer <token>` header.

## Parameters

| Parameter | Type     | In    | Required | Description |
| --------- | -------- | ----- | -------- | ----------- |
| `creator` | `string` | query | ✓        |             |

## Responses

### 200

## Example Usage

### cURL

```bash
curl -X GET "https://frontend-api-v3.pump.fun/livestreams/stream/livestream-token?creator=<creator>" \
  -H "Authorization: Bearer <your_token>" \
  -H "Accept: application/json"
```

### Python

```python
import requests

url = "https://frontend-api-v3.pump.fun/livestreams/stream/livestream-token?creator=<creator>"
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
