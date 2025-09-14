# Pump.fun API Documentation

Complete documentation for all Pump.fun API endpoints and specifications.

## API Versions

[![Frontend API v1 Deprecated](https://img.shields.io/badge/Frontend%20API-v1%20Deprecated-red)](./frontend-api.json)

```bash
https://frontend-api.pump.fun/
```

[![Frontend API v2 Deprecated](https://img.shields.io/badge/Frontend%20API-v2%20Deprecated-red)](./frontend-api-v2.json)

```bash
https://frontend-api-v2.pump.fun/
```

[![Frontend API v3](https://img.shields.io/badge/Frontend%20API-v3-green)](./frontend-api-v3.json)

```bash
https://frontend-api-v3.pump.fun/
```

[![Advanced API v2](https://img.shields.io/badge/Advanced%20Analytics%20API-v2-blue)](./advanced-api-v2.json)

```bash
https://advanced-api-v2.pump.fun/
```

[![Volatility API v2](https://img.shields.io/badge/Volatility%20API-v2-orange)](./volatility-api-v2.json)

```bash
https://volatility-api-v2.pump.fun/
```

## Quick Reference

### Authentication
All APIs require JWT authentication via `Authorization: Bearer <JWT>` header.

### Common Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |
| `Content-Type` | `application/json` | For POST/PUT requests |
| `If-None-Match` | `W/"etag-value"` | For caching |

## Frontend API v3 Endpoints

### Coins
- `POST /coins/mints` - Get metadata for multiple coins
- `GET /coins/top-runners` - Get top performing coins  
- `GET /coins/currently-live` - Get currently live coins
- `GET /coins/for-you` - Get personalized recommendations
- `GET /coins/search` - Search coins with filters
- `GET /coins/user-created-coins/{address}` - Get user's created coins

### Bookmarks
- `GET /bookmarks` - Get user's bookmark collections
- `GET /bookmarks/default` - Get default bookmarks

### Social Features
- `GET /following/{address}` - Get user's following list
- `GET /following/followers/{address}` - Get user's followers
- `GET /following/single/{followId}` - Check follow status

### Meta & Trends
- `GET /metas/current` - Get current trending meta words

## Advanced Analytics API v2 Endpoints

### Coin Analytics
- `GET /coins/list` - Get coins with advanced analytics
- `GET /coins/featured` - Get featured coins with analytics
- `GET /coins/graduated` - Get graduated coins (moved to Raydium)

## Volatility API v2 Endpoints

### Volatility Analysis
- `GET /coins/volatile` - Get most volatile coins by score

## Common Query Parameters

### Pagination
- `offset` (integer) - Starting position (default: 0)
- `limit` (integer) - Number of results (default: varies)

### Filtering
- `includeNsfw` (boolean) - Include NSFW content (default: false)
- `order` (string) - Sort order: `ASC` or `DESC` (default: `DESC`)

### Search
- `searchTerm` (string) - Text query for search
- `sort` (string) - Field to sort by (e.g., `market_cap`, `created_timestamp`)

## Response Formats

### Standard Coin Object
```json
{
  "mint": "string",
  "name": "string", 
  "symbol": "string",
  "description": "string",
  "image_uri": "string",
  "metadata_uri": "string",
  "twitter": "string",
  "telegram": "string",
  "bonding_curve": "string",
  "creator": "string",
  "created_timestamp": "integer",
  "market_cap": "number",
  "usd_market_cap": "number",
  "is_currently_live": "boolean"
}
```

### Advanced Coin Object (Analytics API)
```json
{
  "coinMint": "string",
  "dev": "string",
  "name": "string",
  "ticker": "string",
  "imageUrl": "string",
  "creationTime": "integer",
  "numHolders": "integer",
  "marketCap": "number",
  "volume": "number",
  "bondingCurveProgress": "number",
  "sniperCount": "integer",
  "graduationDate": "integer|null",
  "holders": [
    {
      "totalTokenAmountHeld": "number",
      "isSniper": "boolean",
      "ownedPercentage": "number",
      "holderId": "string"
    }
  ],
  "allTimeHighMarketCap": "number",
  "poolAddress": "string|null",
  "hasTwitter": "boolean",
  "hasTelegram": "boolean",
  "hasWebsite": "boolean",
  "devHoldingsPercentage": "number",
  "buyTransactions": "integer",
  "sellTransactions": "integer",
  "sniperOwnedPercentage": "number",
  "topHoldersPercentage": "number"
}
```

### Volatile Coin Object
```json
{
  "mint": "string",
  "name": "string",
  "symbol": "string",
  "description": "string",
  "created_at": "integer",
  "volatility_score": "number",
  "usd_market_cap": "number",
  "image_uri": "string",
  "metadata_uri": "string",
  "nsfw": "boolean",
  "usd_ath_market_cap": "number",
  "updated_at": "string"
}
```

### Bookmark Response
```json
{
  "id": "string",
  "user_id": "string",
  "name": "string",
  "created_at": "string",
  "items": [
    {
      "item_id": "string",
      "created_at": "string",
      "details": "CoinObject"
    }
  ]
}
```

## Error Handling

### Common Status Codes
- `200 OK` - Success
- `201 Created` - Resource created
- `304 Not Modified` - Content unchanged (caching)
- `400 Bad Request` - Invalid request
- `401 Unauthorized` - Authentication required
- `403 Forbidden` - Access denied
- `404 Not Found` - Resource not found
- `429 Too Many Requests` - Rate limited

### Rate Limiting
- Rate limits vary by endpoint
- Check response headers for limit information:
  - `x-ratelimit-limit` - Request limit
  - `x-ratelimit-remaining` - Remaining requests
  - `x-ratelimit-reset` - Reset time

## Caching

Many endpoints support ETag caching:
- Include `If-None-Match: W/"etag-value"` header
- Returns `304 Not Modified` if content unchanged
- Reduces bandwidth and improves performance

## OpenAPI Specifications
- [Frontend API v1](./frontend-api.json)
- [Frontend API v2](./frontend-api-v2.json)
- [Frontend API v3](./frontend-api-v3.json)

## Detailed Endpoint Documentation
- [POST /coins/mints](./endpoints/POST-coins-mints.md)
- [GET /coins/top-runners](./endpoints/GET-coins-top-runners.md)
- [GET /coins/currently-live](./endpoints/GET-coins-currently-live.md)
- [GET /coins/for-you](./endpoints/GET-coins-for-you.md)
- [GET /coins/search](./endpoints/GET-coins-search.md)
- [GET /coins/user-created-coins/{address}](./endpoints/GET-coins-user-created-coins.md)
- [GET /bookmarks](./endpoints/GET-bookmarks.md)
- [GET /bookmarks/default](./endpoints/GET-bookmarks-default.md)
- [GET /following/{address}](./endpoints/GET-following.md)
- [GET /following/followers/{address}](./endpoints/GET-following-followers.md)
- [GET /following/single/{followId}](./endpoints/GET-following-single.md)
- [GET /metas/current](./endpoints/GET-metas-current.md)
- [GET /coins/list](./endpoints/GET-advanced-coins-list.md)
- [GET /coins/featured](./endpoints/GET-advanced-coins-featured.md)
- [GET /coins/graduated](./endpoints/GET-advanced-coins-graduated.md)
- [GET /coins/volatile](./endpoints/GET-advanced-volatility-coins-volatile.md)

