# GET /clips/{roomName}/{clipId}

## Description
API endpoint for retrieving details of a specific clip from a livestream room.

## Base URL
`https://livestream-api.pump.fun`

## Path Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `roomName` | string | Yes | The room name/identifier for the livestream |
| `clipId` | string | Yes | The unique identifier for the specific clip |

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Accept` | `application/json` | Yes |
| `Origin` | `https://pump.fun` | Yes |

### Example Request
```bash
curl -X GET "https://livestream-api.pump.fun/clips/{roomName}/{clipId}" \
  -H "Accept: application/json" \
  -H "Origin: https://pump.fun"
```

## Response Examples

### Example 1 - Successful Response
**Status:** `200`

**Parameters:**
```json
{
  "roomName": "7Pnqg1S6MYrL6AP1ZXcToTHfdBbTB77ze6Y33qBBpump",
  "clipId": "20250914_135225:535897_20250914_134855-h-0-12000"
}
```

**Response Data:**
```json
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
```

### Example 2 - Clip Not Found
**Status:** `404`

**Parameters:**
```json
{
  "roomName": "invalid-room",
  "clipId": "invalid-clip-id"
}
```

**Response Data:**
```json
{
  "error": "Clip not found"
}
```

**Test Summary:**
- Total test cases: 2
- Successful responses: 1
- Error responses: 1

## Response Fields
| Field | Type | Description |
|-------|------|-------------|
| `roomName` | string | The room name/identifier |
| `clipId` | string | Unique identifier for the clip |
| `sessionId` | string | Session identifier for the livestream |
| `startTime` | string | ISO 8601 timestamp when clip starts |
| `endTime` | string | ISO 8601 timestamp when clip ends |
| `duration` | integer | Duration of clip in seconds |
| `mp4Url` | string | Direct URL to the MP4 video file |
| `mp4S3Key` | string | S3 key for the MP4 file |
| `mp4SizeBytes` | integer | Size of the MP4 file in bytes |
| `mp4CreatedAt` | string | ISO 8601 timestamp when MP4 was created |
| `thumbnailUrl` | string | URL to the thumbnail image |
| `thumbnailS3Key` | string | S3 key for the thumbnail |
| `playlistS3Key` | string | S3 key for playlist (usually empty) |
| `hidden` | boolean | Whether the clip is hidden |
| `clipType` | string | Type of clip (e.g., "HIGHLIGHT") |
| `createdAt` | string | ISO 8601 timestamp when clip was created |
| `highlightCreatorAddress` | string | Wallet address of the user who created the highlight |

## Notes
- This endpoint provides real-time data from the Pump.fun Livestream API
- Response format may vary based on clip availability
- All timestamps are in ISO 8601 format
- Returns detailed information about a specific clip
- The clipId format typically includes timestamp and session information
