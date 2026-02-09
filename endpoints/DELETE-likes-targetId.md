# DELETE /likes/{targetId}

## Endpoint Information

- **URL:** `https://frontend-api-v3.pump.fun/likes/{targetId}`
- **Method:** `DELETE`
- **API:** `frontend-api`
- **Operation ID:** `LikesController_deleteLike`

## Authentication

Requires JWT authentication via `Authorization: Bearer <token>` header.

## Parameters

| Parameter  | Type     | In   | Required | Description |
| ---------- | -------- | ---- | -------- | ----------- |
| `targetId` | `string` | path | ✓        |             |

## Responses

### 200

## Example Usage

### cURL

```bash
curl -X DELETE "https://frontend-api-v3.pump.fun/likes/<targetId>" \
  -H "Authorization: Bearer <your_token>" \
  -H "Accept: application/json"
```

### Python

```python
import requests

url = "https://frontend-api-v3.pump.fun/likes/<targetId>"
headers = {
    "Authorization": "Bearer <your_token>",
    "Accept": "application/json"
}

response = requests.delete(url, headers=headers)
print(response.json())
```

## Notes

- Replace `<your_token>` with your actual JWT token
- Replace path/query parameters with actual values
- Refer to the response schema for expected data structure
