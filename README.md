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

### Core Frontend API v3 Endpoints
- [POST /coins/mints](./endpoints/POST-coins-mints.md) - Fetch metadata for multiple coin mints
- [GET /coins/top-runners](./endpoints/GET-coins-top-runners.md) - Get curated list of top performing coins
- [GET /coins/currently-live](./endpoints/GET-coins-currently-live.md) - Fetch all coins currently live on platform
- [GET /coins/for-you](./endpoints/GET-coins-for-you.md) - Get personalized coin recommendations
- [GET /coins/search](./endpoints/GET-coins-search.md) - Search coins with filtering and sorting
- [GET /coins/user-created-coins/{address}](./endpoints/GET-coins-user-created-coins.md) - Get coins created by specific user
- [GET /bookmarks](./endpoints/GET-bookmarks.md) - Fetch user's bookmarks
- [GET /bookmarks/default](./endpoints/GET-bookmarks-default.md) - Fetch user's default bookmarks
- [GET /following/{address}](./endpoints/GET-following.md) - Get users that a specific user is following
- [GET /following/followers/{address}](./endpoints/GET-following-followers.md) - Get followers of a specific user
- [GET /following/single/{followId}](./endpoints/GET-following-single.md) - Check if user is following another user
- [GET /metas/current](./endpoints/GET-metas-current.md) - Get current trending meta words

### Advanced Analytics API v2 Endpoints
- [GET /coins/list](./endpoints/GET-advanced-coins-list.md) - Advanced coin list with detailed analytics
- [GET /coins/featured](./endpoints/GET-advanced-coins-featured.md) - Featured coins with holder analytics
- [GET /coins/graduated](./endpoints/GET-advanced-coins-graduated.md) - Coins that graduated to Raydium

### Volatility API v2 Endpoints
- [GET /coins/volatile](./endpoints/GET-advanced-volatility-coins-volatile.md) - Most volatile coins by score

## Additional Endpoints

These endpoints have been discovered but are not fully documented or officially supported.

### Authentication & User Management
- [GET /auth/is-admin](./scrapes/GET__auth_is_admin.md)
- [GET /auth/is-super-admin](./scrapes/GET__auth_is_super_admin.md)
- [GET /auth/is-valid-jurisdiction](./scrapes/GET__auth_is_valid_jurisdiction.md)
- [GET /auth/my-profile](./scrapes/GET__auth_my_profile.md)

### Coin Operations
- [GET /coins](./scrapes/GET__coins.md)
- [GET /coins/{mint}](./scrapes/GET__coins__mint_.md)
- [GET /coins/bookmarks/{id}](./scrapes/GET__coins_bookmarks__id_.md)
- [GET /coins/bookmarks/default](./scrapes/GET__coins_bookmarks_default.md)
- [GET /coins/currently-live](./scrapes/GET__coins_currently_live.md)
- [GET /coins/for-you](./scrapes/GET__coins_for_you.md)
- [GET /coins/is-free-coin/{mint}](./scrapes/GET__coins_is_free_coin__mint_.md)
- [GET /coins/king-of-the-hill](./scrapes/GET__coins_king_of_the_hill.md)
- [GET /coins/latest](./scrapes/GET__coins_latest.md)
- [GET /coins/personalized](./scrapes/GET__coins_personalized.md)
- [GET /coins/search](./scrapes/GET__coins_search.md)
- [GET /coins/similar](./scrapes/GET__coins_similar.md)
- [GET /coins/user-created-coins/{userId}](./scrapes/GET__coins_user_created_coins__userId_.md)

### Bookmarks Management
- [GET /bookmarks](./scrapes/GET__bookmarks.md)
- [GET /bookmarks/default](./scrapes/GET__bookmarks_default.md)
- [GET /bookmarks/items/{itemId}](./scrapes/GET__bookmarks_items__itemId_.md)
- [DELETE /bookmarks/{bookmarkId}](./scrapes/DELETE__bookmarks__bookmarkId_.md)
- [DELETE /bookmarks/default/{itemId}](./scrapes/DELETE__bookmarks_default__itemId_.md)

### Trading & Market Data
- [GET /trades/latest](./scrapes/GET__trades_latest.md)
- [GET /trades/followsUserId/count/{mint}](./scrapes/GET__trades_followsUserId_count__mint_.md)
- [GET /sol-price](./scrapes/GET__sol_price.md)

### System & Utilities
- [GET /health](./scrapes/GET__health.md)
- [GET /global-params/{timestamp}](./scrapes/GET__global_params__timestamp_.md)
- [GET /meet](./scrapes/GET__meet.md)
- [GET /vanity-random-mint-public-key](./scrapes/GET__vanity_random_mint_public_key.md)

### Moderation & Content
- [GET /moderation/ban-image-terms](./scrapes/GET__moderation_ban_image_terms.md)
- [GET /moderation/ban-regex-patterns](./scrapes/GET__moderation_ban_regex_patterns.md)
- [GET /moderation/logs](./scrapes/GET__moderation_logs.md)
- [GET /moderation/throttle-exceptions](./scrapes/GET__moderation_throttle_exceptions.md)
- [GET /replies/ban](./scrapes/GET__replies_ban.md)
- [GET /replies/is-origin-of-reply-banned/{id}](./scrapes/GET__replies_is_origin_of_reply_banned__id_.md)
- [GET /replies/user-replies/{address}](./scrapes/GET__replies_user_replies__address_.md)

### Notifications & Social
- [GET /notifications](./scrapes/GET__notifications.md)
- [GET /likes/{targetId}](./scrapes/GET__likes__targetId_.md)

### Media & Content
- [GET /videos/get-previews](./scrapes/GET__videos_get_previews.md)
- [GET /videos/get-signed-url](./scrapes/GET__videos_get_signed_url.md)
- [GET /metas/current](./scrapes/GET__metas_current.md)
- [GET /metas/search](./scrapes/GET__metas_search.md)

### Transaction Processing
- [GET /send-transaction-jito-tip-account](./scrapes/GET__send_transaction_jito_tip_account.md)

### Contributing
If you discover new endpoints or have additional information about existing ones, please contribute by:
1. Testing the endpoint thoroughly
2. Documenting parameters and responses
3. Adding to the appropriate section above

