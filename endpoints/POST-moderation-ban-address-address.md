# POST /moderation/ban/address/{address}

## Endpoint Information

- **URL:** `https://frontend-api-v3.pump.fun/moderation/ban/address/{address}`
- **Method:** `POST`
- **API:** `frontend-api`
- **Operation ID:** `ModerationController_banAddress`

## Authentication

Requires JWT authentication via `Authorization: Bearer <token>` header.

## Parameters

| Parameter | Type     | In   | Required | Description |
| --------- | -------- | ---- | -------- | ----------- |
| `address` | `string` | path | ✓        |             |

## Responses

### 201

## Example Usage

### cURL

```bash
curl -X POST "https://frontend-api-v3.pump.fun/moderation/ban/address/<address>" \
  -H "Authorization: Bearer <your_token>" \
  -H "Accept: application/json"
```

### Python

```python
import requests

url = "https://frontend-api-v3.pump.fun/moderation/ban/address/<address>"
headers = {
    "Authorization": "Bearer <your_token>",
    "Accept": "application/json"
}

response = requests.post(url, headers=headers)
print(response.json())
```

## Notes

- Replace `<your_token>` with your actual JWT token
- Replace path/query parameters with actual values
- Refer to the response schema for expected data structure
