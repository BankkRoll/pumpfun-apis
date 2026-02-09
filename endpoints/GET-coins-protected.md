# GET /coins/protected

## Endpoint Information

- **URL:** `https://frontend-api-v3.pump.fun/coins/protected`
- **Method:** `GET`
- **API:** `frontend-api`
- **Operation ID:** `CoinsController_getAllProtected`

## Authentication

Requires JWT authentication via `Authorization: Bearer <token>` header.

## Parameters

| Parameter     | Type     | In    | Required | Description |
| ------------- | -------- | ----- | -------- | ----------- |
| `limit`       | `number` | query | ✓        |             |
| `offset`      | `number` | query | ✓        |             |
| `sort`        | `string` | query | ✓        |             |
| `searchTerm`  | `string` | query | ✓        |             |
| `order`       | `string` | query | ✓        |             |
| `includeNsfw` | `string` | query | ✓        |             |
| `creator`     | `string` | query | ✓        |             |
| `complete`    | `string` | query | ✓        |             |
| `isLive`      | `string` | query | ✓        |             |
| `fromDate`    | `string` | query | ✓        |             |
| `toDate`      | `string` | query | ✓        |             |
| `banned`      | `string` | query | ✓        |             |

## Responses

### 200

## Example Usage

### cURL

```bash
curl -X GET "https://frontend-api-v3.pump.fun/coins/protected?limit=<limit>&offset=<offset>&sort=<sort>&searchTerm=<searchTerm>&order=<order>&includeNsfw=<includeNsfw>&creator=<creator>&complete=<complete>&isLive=<isLive>&fromDate=<fromDate>&toDate=<toDate>&banned=<banned>" \
  -H "Authorization: Bearer <your_token>" \
  -H "Accept: application/json"
```

### Python

```python
import requests

url = "https://frontend-api-v3.pump.fun/coins/protected?limit=<limit>&offset=<offset>&sort=<sort>&searchTerm=<searchTerm>&order=<order>&includeNsfw=<includeNsfw>&creator=<creator>&complete=<complete>&isLive=<isLive>&fromDate=<fromDate>&toDate=<toDate>&banned=<banned>"
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
