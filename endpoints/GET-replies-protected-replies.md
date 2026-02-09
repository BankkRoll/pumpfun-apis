# GET /replies/protected-replies

## Endpoint Information

- **URL:** `https://frontend-api-v3.pump.fun/replies/protected-replies`
- **Method:** `GET`
- **API:** `frontend-api`
- **Operation ID:** `RepliesController_getProtectedReplies`

## Authentication

Requires JWT authentication via `Authorization: Bearer <token>` header.

## Parameters

| Parameter     | Type     | In    | Required | Description |
| ------------- | -------- | ----- | -------- | ----------- |
| `limit`       | `string` | query | ✓        |             |
| `offset`      | `string` | query | ✓        |             |
| `sortBy`      | `string` | query | ✓        |             |
| `order`       | `string` | query | ✓        |             |
| `address`     | `string` | query | ✓        |             |
| `searchQuery` | `string` | query | ✓        |             |
| `searchCA`    | `string` | query | ✓        |             |
| `searchUA`    | `string` | query | ✓        |             |
| `hidden`      | `string` | query | ✓        |             |
| `banned`      | `string` | query | ✓        |             |
| `fromDate`    | `string` | query | ✓        |             |
| `toDate`      | `string` | query | ✓        |             |
| `hasImage`    | `string` | query | ✓        |             |
| `isScam`      | `string` | query | ✓        |             |
| `isSpam`      | `string` | query | ✓        |             |

## Responses

### 200

## Example Usage

### cURL

```bash
curl -X GET "https://frontend-api-v3.pump.fun/replies/protected-replies?limit=<limit>&offset=<offset>&sortBy=<sortBy>&order=<order>&address=<address>&searchQuery=<searchQuery>&searchCA=<searchCA>&searchUA=<searchUA>&hidden=<hidden>&banned=<banned>&fromDate=<fromDate>&toDate=<toDate>&hasImage=<hasImage>&isScam=<isScam>&isSpam=<isSpam>" \
  -H "Authorization: Bearer <your_token>" \
  -H "Accept: application/json"
```

### Python

```python
import requests

url = "https://frontend-api-v3.pump.fun/replies/protected-replies?limit=<limit>&offset=<offset>&sortBy=<sortBy>&order=<order>&address=<address>&searchQuery=<searchQuery>&searchCA=<searchCA>&searchUA=<searchUA>&hidden=<hidden>&banned=<banned>&fromDate=<fromDate>&toDate=<toDate>&hasImage=<hasImage>&isScam=<isScam>&isSpam=<isSpam>"
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
