# GET /clips/{roomName}

## Description
API endpoint for retrieving clips from a specific livestream room.

## Base URL
`https://livestream-api.pump.fun`

## Path Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `roomName` | string | Yes | The room name/identifier for the livestream |

## Query Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `limit` | integer | No | Maximum number of clips to return (default: 20) |
| `clipType` | string | No | Filter clips by type (e.g., "HIGHLIGHT") |

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |

### Example Request
```bash
curl -X GET "https://livestream-api.pump.fun/clips/{roomName}?limit=20&clipType=HIGHLIGHT" \
  -H "Authorization: Bearer YOUR_JWT_TOKEN"
```

## Response Examples

### Example 1 - Successful Response
**Status:** `200`

**Parameters:**
```json
{
  "roomName": "7Pnqg1S6MYrL6AP1ZXcToTHfdBbTB77ze6Y33qBBpump",
  "limit": 20,
  "clipType": "HIGHLIGHT"
}
```

**Response Data:**
```json
{
  "clips": [
    {
      "roomName": "7Pnqg1S6MYrL6AP1ZXcToTHfdBbTB77ze6Y33qBBpump",
      "clipId": "20250914_135225:535897_20250914_134855-h-0-12000",
      "sessionId": "535897_20250914_134855",
      "startTime": "2025-09-14T13:52:25.735Z",
      "endTime": "2025-09-14T13:52:37.735Z",
      "duration": 12,
      "mp4Url": "https://clips.pump.fun/7Pnqg1S6MYrL6AP1ZXcToTHfdBbTB77ze6Y33qBBpump/clips/20250914_135225:535897_20250914_134855-h-0-12000/clip.mp4",
      "mp4S3Key": "7Pnqg1S6MYrL6AP1ZXcToTHfdBbTB77ze6Y33qBBpump/clips/20250914_135225:535897_20250914_134855-h-0-12000/clip.mp4",
      "mp4SizeBytes": 1267218,
      "mp4CreatedAt": "2025-09-14T13:52:59.15257124Z",
      "thumbnailUrl": "https://clips.pump.fun/7Pnqg1S6MYrL6AP1ZXcToTHfdBbTB77ze6Y33qBBpump/clips/20250914_135225:535897_20250914_134855/thumbnail.jpg",
      "thumbnailS3Key": "7Pnqg1S6MYrL6AP1ZXcToTHfdBbTB77ze6Y33qBBpump/clips/20250914_135225:535897_20250914_134855/thumbnail.jpg",
      "playlistS3Key": "",
      "hidden": false,
      "clipType": "HIGHLIGHT",
      "createdAt": "2025-09-14T13:52:59.15257124Z",
      "highlightCreatorAddress": "CtdbZzdzLseJoYwcphD3niF8E6Ah4HaUXb5LgUt9iqc2"
    }
  ]
}
```

**Test Summary:**
- Total test cases: 1
- Successful responses: 1
- Error responses: 0

## Response Fields
| Field | Type | Description |
|-------|------|-------------|
| `clips` | array | Array of clip objects |
| `clips[].roomName` | string | The room name/identifier |
| `clips[].clipId` | string | Unique identifier for the clip |
| `clips[].sessionId` | string | Session identifier for the livestream |
| `clips[].startTime` | string | ISO 8601 timestamp when clip starts |
| `clips[].endTime` | string | ISO 8601 timestamp when clip ends |
| `clips[].duration` | integer | Duration of clip in seconds |
| `clips[].mp4Url` | string | Direct URL to the MP4 video file |
| `clips[].mp4S3Key` | string | S3 key for the MP4 file |
| `clips[].mp4SizeBytes` | integer | Size of the MP4 file in bytes |
| `clips[].mp4CreatedAt` | string | ISO 8601 timestamp when MP4 was created |
| `clips[].thumbnailUrl` | string | URL to the thumbnail image |
| `clips[].thumbnailS3Key` | string | S3 key for the thumbnail |
| `clips[].playlistS3Key` | string | S3 key for playlist (usually empty) |
| `clips[].hidden` | boolean | Whether the clip is hidden |
| `clips[].clipType` | string | Type of clip (e.g., "HIGHLIGHT") |
| `clips[].createdAt` | string | ISO 8601 timestamp when clip was created |
| `clips[].highlightCreatorAddress` | string | Wallet address of the user who created the highlight |

## Notes
- This endpoint provides real-time data from the Pump.fun Livestream API
- Response format may vary based on parameters and room availability
- All timestamps are in ISO 8601 format
- Clips are typically short video segments from livestreams
- The `clipType` parameter can filter for specific types of clips like highlights
