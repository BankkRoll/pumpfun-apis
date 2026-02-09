# GET /coins

## Endpoint Information

- **URL:** `https://frontend-api-v3.pump.fun/coins`
- **Method:** `GET`
- **API:** `frontend-api`
- **Operation ID:** `CoinsController_getAll`

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

## Responses

### 200

## Example Usage

### cURL

```bash
curl -X GET "https://frontend-api-v3.pump.fun/coins?limit=<limit>&offset=<offset>&sort=<sort>&searchTerm=<searchTerm>&order=<order>&includeNsfw=<includeNsfw>&creator=<creator>&complete=<complete>&meta=<meta>" \
  -H "Authorization: Bearer <your_token>" \
  -H "Accept: application/json"
```

### Python

```python
import requests

url = "https://frontend-api-v3.pump.fun/coins?limit=<limit>&offset=<offset>&sort=<sort>&searchTerm=<searchTerm>&order=<order>&includeNsfw=<includeNsfw>&creator=<creator>&complete=<complete>&meta=<meta>"
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
