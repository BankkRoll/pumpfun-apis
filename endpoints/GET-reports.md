# GET /reports

## Endpoint Information

- **URL:** `https://frontend-api-v3.pump.fun/reports`
- **Method:** `GET`
- **API:** `frontend-api`
- **Operation ID:** `ReportsController_getReports`

## Authentication

Requires JWT authentication via `Authorization: Bearer <token>` header.

## Parameters

| Parameter         | Type     | In    | Required | Description |
| ----------------- | -------- | ----- | -------- | ----------- |
| `limit`           | `number` | query | ✓        |             |
| `offset`          | `number` | query | ✓        |             |
| `type`            | `string` | query | ✓        |             |
| `done`            | `string` | query | ✓        |             |
| `createdAtFrom`   | `string` | query | ✓        |             |
| `createdAtTo`     | `string` | query | ✓        |             |
| `isCurrentlyLive` | `string` | query | ✓        |             |

## Responses

### 200

## Example Usage

### cURL

```bash
curl -X GET "https://frontend-api-v3.pump.fun/reports?limit=<limit>&offset=<offset>&type=<type>&done=<done>&createdAtFrom=<createdAtFrom>&createdAtTo=<createdAtTo>&isCurrentlyLive=<isCurrentlyLive>" \
  -H "Authorization: Bearer <your_token>" \
  -H "Accept: application/json"
```

### Python

```python
import requests

url = "https://frontend-api-v3.pump.fun/reports?limit=<limit>&offset=<offset>&type=<type>&done=<done>&createdAtFrom=<createdAtFrom>&createdAtTo=<createdAtTo>&isCurrentlyLive=<isCurrentlyLive>"
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
