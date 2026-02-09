# GET /coins/search

## Endpoint Information

- **URL:** `https://frontend-api-v3.pump.fun/coins/search`
- **Method:** `GET`
- **API:** `frontend-api`
- **Operation ID:** `CoinsController_search`

## Authentication

Requires JWT authentication via `Authorization: Bearer <token>` header.

## Parameters

| Parameter     | Type      | In    | Required | Description |
| ------------- | --------- | ----- | -------- | ----------- |
| `limit`       | `number`  | query | ✓        |             |
| `offset`      | `number`  | query | ✓        |             |
| `sort`        | `string`  | query | ✓        |             |
| `searchTerm`  | `string`  | query | ✓        |             |
| `order`       | `string`  | query | ✓        |             |
| `includeNsfw` | `boolean` | query | ✓        |             |
| `creator`     | `string`  | query | ✓        |             |
| `complete`    | `boolean` | query | ✓        |             |
| `meta`        | `string`  | query | ✓        |             |
| `type`        | `string`  | query | ✓        |             |

## Responses

### 200

## Example Usage

### cURL

```bash
curl -X GET "https://frontend-api-v3.pump.fun/coins/search?limit=<limit>&offset=<offset>&sort=<sort>&searchTerm=<searchTerm>&order=<order>&includeNsfw=<includeNsfw>&creator=<creator>&complete=<complete>&meta=<meta>&type=<type>" \
  -H "Authorization: Bearer <your_token>" \
  -H "Accept: application/json"
```

### Python

```python
import requests

url = "https://frontend-api-v3.pump.fun/coins/search?limit=<limit>&offset=<offset>&sort=<sort>&searchTerm=<searchTerm>&order=<order>&includeNsfw=<includeNsfw>&creator=<creator>&complete=<complete>&meta=<meta>&type=<type>"
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
