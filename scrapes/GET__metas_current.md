# GET /metas/current

## Description
API endpoint for trending meta words and topics.

## Base URL
`https://frontend-api-v3.pump.fun`

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |

### Example Request
```bash
curl -X GET "https://frontend-api-v3.pump.fun/metas/current" \
  -H "Authorization: Bearer YOUR_JWT_TOKEN"
```

## Response Examples

### Example 1
**Status:** `200`

**Response Data:**
```json
{
  "0": {
    "word": "Streamer Life",
    "word_with_strength": "🔥🔥Streamer Life🎥",
    "score": 230
  },
  "1": {
    "word": "KAPPA Wave",
    "word_with_strength": "🔥KAPPA Wave😏",
    "score": 80
  },
  "2": {
    "word": "PUMPCYCLE",
    "word_with_strength": "🔥PUMPCYCLE🔁",
    "score": 72
  },
  "3": {
    "word": "SGUY Universe",
    "word_with_strength": "🔥SGUY Universe🦸‍♂️",
    "score": 70
  },
  "4": {
    "word": "Animal Squad",
    "word_with_strength": "🔥Animal Squad🦴",
    "score": 49
  },
  "5": {
    "word": "Justice Moves",
    "word_with_strength": "🔥Justice Moves⚖️",
    "score": 27
  },
  "6": {
    "word": "DIDDY Run",
    "word_with_strength": "DIDDY Run🚀",
    "score": 21
  },
  "7": {
    "word": "Clout Chasers",
    "word_with_strength": "Clout Chasers💸",
    "score": 18
  },
  "8": {
    "word": "MAXXING",
    "word_with_strength": "MAXXING💪",
    "score": 17
  },
  "9": {
    "word": "Bad Luck Ricky",
    "word_with_strength": "Bad Luck Ricky🥊",
    "score": 12
  },
  "...": "... and 2 more properties"
}
```

## Response Fields
| Field | Type | Description |
|-------|------|-------------|
| `status` | integer | HTTP status code |
| `data` | object | Response data (varies by endpoint) |

## Notes
- This endpoint provides real-time data from the Pump.fun API
- Response format may vary based on parameters and authentication
- All timestamps are in UNIX format unless otherwise specified
