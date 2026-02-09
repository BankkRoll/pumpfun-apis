# GET /moderation/ban-users

## Endpoint Information

- **URL:** `https://frontend-api-v3.pump.fun/moderation/ban-users`
- **Method:** `GET`
- **API:** `frontend-api`
- **Operation ID:** `ModerationController_getBanUsers`

## Authentication

Requires JWT authentication via `Authorization: Bearer <token>` header.

## Parameters

| Parameter      | Type     | In    | Required | Description |
| -------------- | -------- | ----- | -------- | ----------- |
| `limit`        | `string` | query | ✓        |             |
| `offset`       | `string` | query | ✓        |             |
| `sortBy`       | `string` | query | ✓        |             |
| `order`        | `string` | query | ✓        |             |
| `searchQuery`  | `string` | query | ✓        |             |
| `active`       | `string` | query | ✓        |             |
| `unbanRequest` | `string` | query | ✓        |             |
| `fromDate`     | `string` | query | ✓        |             |
| `toDate`       | `string` | query | ✓        |             |

## Responses

### 200

## Example Usage

### cURL

```bash
curl -X GET "https://frontend-api-v3.pump.fun/moderation/ban-users?limit=<limit>&offset=<offset>&sortBy=<sortBy>&order=<order>&searchQuery=<searchQuery>&active=<active>&unbanRequest=<unbanRequest>&fromDate=<fromDate>&toDate=<toDate>" \
  -H "Authorization: Bearer <your_token>" \
  -H "Accept: application/json"
```

### Python

```python
import requests

url = "https://frontend-api-v3.pump.fun/moderation/ban-users?limit=<limit>&offset=<offset>&sortBy=<sortBy>&order=<order>&searchQuery=<searchQuery>&active=<active>&unbanRequest=<unbanRequest>&fromDate=<fromDate>&toDate=<toDate>"
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
