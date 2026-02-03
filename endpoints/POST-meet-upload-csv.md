# POST /meet/upload-csv

## Endpoint Information

- **URL:** `https://frontend-api-v2.pump.fun/meet/upload-csv`
- **Method:** `POST`
- **API:** `frontend-api-v2`
- **Operation ID:** `InterviewController_uploadCsv`

## Authentication

Requires JWT authentication via `Authorization: Bearer <token>` header.

## Parameters

*None*

## Responses

### 201
## Example Usage

### cURL

```bash
curl -X POST "https://frontend-api-v2.pump.fun/meet/upload-csv" \
  -H "Authorization: Bearer <your_token>" \
  -H "Accept: application/json"
```

### Python

```python
import requests

url = "https://frontend-api-v2.pump.fun/meet/upload-csv"
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