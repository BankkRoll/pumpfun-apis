# GET /following/followers/{address}

## Description
Fetch all followers of a specific user.

## Base URL
`https://frontend-api-v3.pump.fun`

## Path Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `address` | string | Yes | User's wallet address |

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |

## Response
**Status:** `200 OK`

```json
[
  {
    "username": "stfubb",
    "profile_image": null,
    "address": "F6rGFZvEwdTrjPbPF7g9z8P6C6XiVbbA5JDz1eTdnL7B",
    "timestamp": 1749176899119,
    "followers": 542
  },
  {
    "username": "rodrigo1",
    "profile_image": "https://ipfs.io/ipfs/Qmf9Qh9bHv2D8qxoKHWdCvS3boAjHkP45UKyrStvm2zJ8C",
    "address": "HGtT3hvJyk8XjB9Js8JRcdbSezXpQwZ5cGcAH89pz4Zc",
    "timestamp": 1748864517408,
    "followers": 403
  },
  {
    "username": "gopnut",
    "profile_image": "https://ipfs.io/ipfs/Qmegt1BZugHNyDLXsWLF5JZx2FtWgiPTzpNKaUPnjeSbk6",
    "address": "E49Jz5YBTpFy53TzTitnYJRHjc9xVKnGtk2JoksudWmt",
    "timestamp": 1738424773368,
    "followers": 325
  }
]
```

## Response Fields
| Field | Type | Description |
|-------|------|-------------|
| `username` | string | Follower's username |
| `profile_image` | string/null | URL to follower's profile image |
| `address` | string | Follower's wallet address |
| `timestamp` | integer | UNIX timestamp when they started following |
| `followers` | integer | Number of followers this user has |
