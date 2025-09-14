# GET /videos/get-signed-url

## Description
API endpoint for /videos/get-signed-url operations.

## Base URL
`https://frontend-api-v3.pump.fun`

## Query Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `extension` | string | Yes | No description available |

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |

### Example Request
```bash
curl -X GET "https://frontend-api-v3.pump.fun/videos/get-signed-url" \
  -H "Authorization: Bearer YOUR_JWT_TOKEN"
```

## Response Examples

### Example 1
**Status:** `200`

**Parameters:**
```json
{
  "extension": "mp4"
}
```

**Response Data:**
```json
{
  "filename": "6086bb847f6f9ef65dadd8c7e3de5dcd62f1704817a43cfc760eae1bc660c533.mp4",
  "url": {
    "url": "https://s3.us-east-1.amazonaws.com/media.pump.fun",
    "fields": {
      "Content-type": "video/mp4",
      "bucket": "media.pump.fun",
      "X-Amz-Algorithm": "AWS4-HMAC-SHA256",
      "X-Amz-Credential": "AKIAQMEY5U7ZHWO4R24X/20250914/us-east-1/s3/aws4_request",
      "X-Amz-Date": "20250914T141140Z",
      "key": "videos/6086bb847f6f9ef65dadd8c7e3de5dcd62f1704817a43cfc760eae1bc660c533.mp4",
      "Policy": "eyJleHBpcmF0aW9uIjoiMjAyNS0wOS0xNFQxNDoyNjo0MFoiLCJjb25kaXRpb25zIjpbWyJjb250ZW50LWxlbmd0aC1yYW5nZSIsMCwxMDQ4NTc2MF0seyJDb250ZW50LXR5cGUiOiJ2aWRlby9tcDQifSx7ImJ1Y2tldCI6Im1lZGlhLnB1bXAuZnVuIn0seyJYLUFtei1BbGdvcml0aG0iOiJBV1M0LUhNQUMtU0hBMjU2In0seyJYLUFtei1DcmVkZW50aWFsIjoiQUtJQVFNRVk1VTdaSFdPNFIyNFgvMjAyNTA5MTQvdXMtZWFzdC0xL3MzL2F3czRfcmVxdWVzdCJ9LHsiWC1BbXotRGF0ZSI6IjIwMjUwOTE0VDE0MTE0MFoifSx7ImtleSI6InZpZGVvcy82MDg2YmI4NDdmNmY5ZWY2NWRhZGQ4YzdlM2RlNWRjZDYyZjE3MDQ4MTdhNDNjZmM3NjBlYWUxYmM2NjBjNTMzLm1wNCJ9XX0=",
      "X-Amz-Signature": "92c2f803cc055d8cc2d87b04a45da83fbf91b693712ac17ba652fb262538b3d7"
    }
  }
}
```

**Test Summary:**
- Total test cases: 4
- Successful responses: 4
- Error responses: 0

## Response Fields
| Field | Type | Description |
|-------|------|-------------|
| `status` | integer | HTTP status code |
| `data` | object | Response data (varies by endpoint) |

## Notes
- This endpoint provides real-time data from the Pump.fun API
- Response format may vary based on parameters and authentication
- All timestamps are in UNIX format unless otherwise specified
