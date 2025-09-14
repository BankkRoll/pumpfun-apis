# GET /metas/current

## Description
Fetch a list of current trending "meta words" on the platform.

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

## Response
**Status:** `200 OK`

```json
[
  {
    "word": "Streamer Life",
    "word_with_strength": "🔥Streamer Life🎥",
    "score": 507
  },
  {
    "word": "Bad Luck Ricky",
    "word_with_strength": "🔥Bad Luck Ricky🦊",
    "score": 128
  },
  {
    "word": "PUMPCYCLE",
    "word_with_strength": "🔥PUMPCYCLE🔁",
    "score": 105
  },
  {
    "word": "KAPPA Wave",
    "word_with_strength": "🔥KAPPA Wave😏",
    "score": 91
  },
  {
    "word": "Animal Squad",
    "word_with_strength": "🔥Animal Squad🦴",
    "score": 71
  }
]
```

## Response Fields
| Field | Type | Description |
|-------|------|-------------|
| `word` | string | Raw meta word or phrase |
| `word_with_strength` | string | Display version with symbols/emojis for emphasis |
| `score` | integer | Popularity score or strength of the meta word |
