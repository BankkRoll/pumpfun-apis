# Pump.fun API Documentation

Complete documentation for all Pump.fun API endpoints and specifications.

**Total Documented Endpoints: 483**

See the [endpoints/](endpoints/) folder for complete endpoint documentation or browse the [INDEX.md](endpoints/INDEX.md) for a full list.

## API Versions

### Frontend API v3 (Current)

[![Frontend API v3](https://img.shields.io/badge/Frontend%20API-v3-green)](./discovered/frontend-api-v3.json)

```bash
https://frontend-api-v3.pump.fun/
```

### Frontend API v2 (Deprecated)

[![Frontend API v2 Deprecated](https://img.shields.io/badge/Frontend%20API-v2%20Deprecated-red)](./discovered/frontend-api-v2.json)

```bash
https://frontend-api-v2.pump.fun/
```

### Frontend API v1 (Deprecated)

[![Frontend API v1 Deprecated](https://img.shields.io/badge/Frontend%20API-v1%20Deprecated-red)](./discovered/frontend-api.json)

```bash
https://frontend-api.pump.fun/
```

### Advanced Analytics API v2

[![Advanced API v2](https://img.shields.io/badge/Advanced%20Analytics%20API-v2-blue)](./discovered/advanced-api-v2.json)

```bash
https://advanced-api-v2.pump.fun/
```

### Other Discovered API Domains

The spider has discovered these additional API domains (OpenAPI specs not available):

- `https://profile-api.pump.fun` - User profile operations
- `https://swap-api.pump.fun` - Token swap functionality
- `https://volatility-api-v2.pump.fun` - Volatility metrics
- `https://clips-api.pump.fun` - Livestream clips
- `https://market-api.pump.fun` - Market data

## Quick Reference

### Authentication

Most APIs require JWT authentication via `Authorization: Bearer <JWT>` header. It's recommended to include authentication with all requests to ensure complete data retrieval and avoid potential access issues.

### Common Headers

| Header          | Value                       | Required              |
| --------------- | --------------------------- | --------------------- |
| `Authorization` | `Bearer <JWT>`              | Yes                   |
| `Accept`        | `application/json` or `*/*` | Yes                   |
| `Origin`        | `https://pump.fun`          | Yes                   |
| `Content-Type`  | `application/json`          | For POST/PUT requests |
| `If-None-Match` | `W/"etag-value"`            | For caching           |

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

All OpenAPI specs are located in the [discovered/](discovered/) folder:

- [Frontend API v1](./discovered/frontend-api.json)
- [Frontend API v2](./discovered/frontend-api-v2.json)
- [Frontend API v3](./discovered/frontend-api-v3.json)
- [Advanced Analytics API v2](./discovered/advanced-api-v2.json)

## Documentation

All 483 endpoints are documented in the [endpoints/](endpoints/) folder with complete details including:

- Full URL and method
- Authentication requirements
- Parameters and request body schemas
- Response information
- Code examples in cURL and Python

Browse by endpoint type:

- [GET Endpoints](./endpoints/INDEX.md#get-endpoints)
- [POST Endpoints](./endpoints/INDEX.md#post-endpoints)
- [PUT Endpoints](./endpoints/INDEX.md#put-endpoints)
- [DELETE Endpoints](./endpoints/INDEX.md#delete-endpoints)
- [PATCH Endpoints](./endpoints/INDEX.md#patch-endpoints)

---

## Disclaimer

This is an **unofficial repository** that documents publicly available Pump.fun API endpoints.

- All APIs and services referenced are **owned and operated by Pump.fun**.
- This documentation is provided **for research and educational purposes only**.
- I **do not endorse, support, or encourage** spam, abuse, or misuse of these endpoints.
- Please respect rate limits, authentication, and Pump.fun's terms of service.

If you are a Pump.fun operator or authorized representative and want content **removed, corrected, or updated**, please **open an issue** in this repository. I will review and respond promptly.

Licensed under the [MIT License](./LICENSE).
