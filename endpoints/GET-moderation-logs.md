# GET /moderation/logs

## Endpoint Information

- **URL:** `https://frontend-api-v3.pump.fun/moderation/logs`
- **Method:** `GET`
- **API:** `frontend-api`
- **Operation ID:** `ModerationController_getLogs`

## Authentication

Requires JWT authentication via `Authorization: Bearer <token>` header.

## Parameters

| Parameter   | Type     | In    | Required | Description |
| ----------- | -------- | ----- | -------- | ----------- |
| `offset`    | `number` | query | ✓        |             |
| `limit`     | `number` | query | ✓        |             |
| `moderator` | `string` | query | ✓        |             |

## Responses

### 200

## Example Usage

### cURL

```bash
curl -X GET "https://frontend-api-v3.pump.fun/moderation/logs?offset=<offset>&limit=<limit>&moderator=<moderator>" \
  -H "Authorization: Bearer <your_token>" \
  -H "Accept: application/json"
```

### Python

```python
import requests

url = "https://frontend-api-v3.pump.fun/moderation/logs?offset=<offset>&limit=<limit>&moderator=<moderator>"
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
