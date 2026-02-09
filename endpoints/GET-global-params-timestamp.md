# GET /global-params/{timestamp}

## Endpoint Information

- **URL:** `https://frontend-api-v3.pump.fun/global-params/{timestamp}`
- **Method:** `GET`
- **API:** `frontend-api`
- **Operation ID:** `GlobalParamsController_getGlobalParamsByTimestamp`

## Authentication

Requires JWT authentication via `Authorization: Bearer <token>` header.

## Parameters

| Parameter   | Type     | In   | Required | Description |
| ----------- | -------- | ---- | -------- | ----------- |
| `timestamp` | `number` | path | ✓        |             |

## Responses

### 200

## Example Usage

### cURL

```bash
curl -X GET "https://frontend-api-v3.pump.fun/global-params/<timestamp>" \
  -H "Authorization: Bearer <your_token>" \
  -H "Accept: application/json"
```

### Python

```python
import requests

url = "https://frontend-api-v3.pump.fun/global-params/<timestamp>"
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
