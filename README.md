# API Documentation

This document outlines the endpoints available in pumpfun API.


## Table of Contents

  - [Base URL](#base-url)
  - [Trades](#trades)
  - [Coins](#coins)
  - [Authentication](#authentication)
  - [Moderation](#moderation)
  - [Replies](#replies)
  - [Users](#users)
  - [Likes and Following](#likes-and-following)
  - [Livestreams](#livestreams)
  - [Reports](#reports)
  - [Activity](#activity)
  - [Bookmarks](#bookmarks)
  - [Other Features](#other-features)
  - [Data Transfer Objects (DTOs)](#data-transfer-objects-dtos)

## Endpoints

[![Frontend API v1 Deprecated](https://img.shields.io/badge/Frontend%20API-v1%20Deprecated-red)](./frontend-api.json)

```bash
https://frontend-api.pump.fun/
```

[![Frontend API v2](https://img.shields.io/badge/Frontend%20API-v2-blue)](./frontend-api-v2.json)

```bash
https://frontend-api-v2.pump.fun/
```

[![Frontend API v3](https://img.shields.io/badge/Frontend%20API-v3-green)](./frontend-api-v3.json)

```bash
https://frontend-api-v3.pump.fun/
```

## Trades

- `GET /trades/latest`: Retrieve the latest trades
- `GET /trades/all/{mint}`: Get all trades for a specific mint
- `POST /trades/signatures`: Submit trade signatures
- `POST /trades/signatures/small`: Submit small trade signatures
- `GET /trades/count/{mint}`: Get trade count for a specific mint
- `GET /trades/followsUserId/{mint}`: Get trades following a user for a specific mint
- `GET /trades/followsUserId/count/{mint}`: Get count of trades following a user for a specific mint

## Coins

- `POST /coins/sign-create-tx`: Sign a create transaction for a coin
- `POST /coins/create`: Create a new coin
- `GET /coins/king-of-the-hill`: Get the current "king of the hill" coin
- `GET /coins/currently-live`: Get currently live coins
- `GET /coins/for-you`: Get personalized coin recommendations
- `GET /coins/featured/{timeWindow}`: Get featured coins within a time window
- `GET /coins/user-created-coins/{userId}`: Get coins created by a specific user
- `GET /coins/bookmarks/default`: Get default coin bookmarks
- `GET /coins/is-free-coin/{mint}`: Check if a coin is free
- `GET /coins/latest`: Get the latest coins
- `GET /coins/protected`: Get protected coins
- `GET /coins/personalized`: Get personalized coin list
- `GET /coins/similar`: Get similar coins
- `GET /coins/search`: Search for coins
- `GET /coins/{mint}`: Get details of a specific coin
- `GET /coins`: Get a list of coins
- `PATCH /coins/ban/{mint}`: Ban a specific coin

## Authentication

- `GET /auth/is-admin`: Check if the user is an admin
- `GET /auth/is-super-admin`: Check if the user is a super admin
- `POST /auth/login`: User login
- `GET /auth/my-profile`: Get current user's profile
- `GET /auth/is-valid-jurisdiction`: Check if the jurisdiction is valid
- `POST /auth/logout`: User logout

## Moderation

- `GET /moderation/logs`: Get moderation logs
- `POST /moderation/ban/address/{address}`: Ban a specific address
- `POST /moderation/mark-as-nsfw/{mint}`: Mark a mint as NSFW
- `POST /moderation/bulk-nsfw`: Bulk mark as NSFW
- `POST /moderation/mark-as-hidden/{id}`: Mark an item as hidden
- `POST /moderation/bulk-hidden`: Bulk mark as hidden
- `POST /moderation/ban/{id}`: Ban a specific item
- `POST /moderation/bulk-ban`: Bulk ban items
- `POST /moderation/ban-terms`: Add ban terms
- `GET /moderation/ban-terms`: Get ban terms
- `POST /moderation/ban-image-terms`: Add image ban terms
- `GET /moderation/ban-image-terms`: Get image ban terms
- `POST /moderation/ban-regex-patterns`: Add regex ban patterns
- `GET /moderation/ban-regex-patterns`: Get regex ban patterns
- `POST /moderation/add-throttle-exception`: Add a throttle exception
- `GET /moderation/throttle-exceptions`: Get throttle exceptions
- `DELETE /moderation/ban-terms/{id}`: Delete a ban term
- `DELETE /moderation/ban-image-terms/{id}`: Delete an image ban term
- `DELETE /moderation/ban-regex-patterns/{id}`: Delete a regex ban pattern
- `DELETE /moderation/delete-throttle-exception/{id}`: Delete a throttle exception
- `GET /moderation/ban`: Get ban list
- `GET /moderation/ban-users`: Get banned users
- `GET /moderation/moderated-comments`: Get moderated comments
- `GET /moderation/moderated-reports`: Get moderated reports
- `POST /moderation/mark-as-ignored/{id}`: Mark an item as ignored
- `POST /moderation/delete-photo/{mint}`: Delete a photo for a specific mint

## Replies

- `POST /replies`: Create a new reply
- `GET /replies`: Get replies
- `GET /replies/ban`: Get banned replies
- `GET /replies/protected-replies`: Get protected replies
- `GET /replies/{mint}`: Get replies for a specific mint
- `POST /replies/mints`: Get replies for multiple mints
- `GET /replies/user-replies/{address}`: Get replies for a specific user
- `GET /replies/is-origin-of-reply-banned/{id}`: Check if the origin of a reply is banned
- `POST /replies/experimental`: Experimental reply endpoint

## Users

- `GET /users/{id}`: Get user information
- `POST /users/register`: Register a new user
- `POST /users`: Create a new user
- `DELETE /users`: Delete a user

## Likes and Following

- `POST /likes/{targetId}`: Like a target
- `DELETE /likes/{targetId}`: Unlike a target
- `GET /likes/{targetId}`: Get likes for a target
- `POST /following/{userId}`: Follow a user
- `DELETE /following/{userId}`: Unfollow a user
- `GET /following/{userId}`: Get following status
- `POST /following/v2/{userId}`: Follow a user (v2)
- `GET /following/single/{id}`: Get single following status
- `GET /following/followers/{id}`: Get followers of a user
- `GET /following/mutuals/{id}`: Get mutual followers

## Livestreams

- `GET /livestreams/{mint}`: Get livestream information
- `GET /livestreams/{mint}/raw`: Get raw livestream data
- `GET /livestreams/livekit/token/host`: Get LiveKit host token
- `GET /livestreams/livekit/token/participant`: Get LiveKit participant token
- `POST /livestreams/livekit/raise-hand`: Raise hand in LiveKit
- `POST /livestreams/livekit/invite-to-stage`: Invite to stage in LiveKit
- `POST /livestreams/livekit/remove-from-stage`: Remove from stage in LiveKit
- `GET /livestreams/stream/livestream-token`: Get livestream token
- `GET /livestreams/stream/livechat-token`: Get live chat token
- `POST /livestreams/stream/livechat-channel/{mint}`: Create live chat channel
- `POST /livestreams/create-livestream`: Create a new livestream
- `PUT /livestreams/update-livestream`: Update a livestream
- `PUT /livestreams/{mint}/disable-livestream`: Disable a livestream
- `PUT /livestreams/{mint}/enable-livestream`: Enable a livestream
- `PUT /livestreams/{mint}/unban-livestream`: Unban a livestream
- `PUT /livestreams/{mint}/ban-livestream`: Ban a livestream
- `POST /livestreams/call-webhook`: Call livestream webhook
- `POST /livestreams/livekit-webhook`: LiveKit webhook endpoint

## Reports

- `POST /reports`: Create a new report
- `GET /reports`: Get reports
- `POST /reports/update`: Update a report
- `DELETE /reports/{id}`: Delete a report
- `POST /reports/reportComment`: Report a comment

## Activity

- `POST /activity/click`: Log a click activity
- `POST /activity/convert`: Log a conversion activity
- `POST /activity/seen`: Log a seen activity
- `POST /activity/click-advanced`: Log an advanced click activity
- `POST /activity/convert-advanced`: Log an advanced conversion activity
- `POST /activity/seen-advanced`: Log an advanced seen activity

## Bookmarks

- `POST /bookmarks`: Create a new bookmark
- `GET /bookmarks`: Get bookmarks
- `GET /bookmarks/default`: Get default bookmarks
- `GET /bookmarks/{bookmarkId}`: Get a specific bookmark
- `PUT /bookmarks/{bookmarkId}`: Update a bookmark
- `DELETE /bookmarks/{bookmarkId}`: Delete a bookmark
- `POST /bookmarks/items/add`: Add an item to bookmarks
- `POST /bookmarks/items/remove`: Remove an item from bookmarks
- `POST /bookmarks/default/items`: Add items to default bookmark
- `POST /bookmarks/{bookmarkId}/items`: Add items to a specific bookmark
- `GET /bookmarks/items/{itemId}`: Get a bookmarked item
- `DELETE /bookmarks/default/{itemId}`: Remove an item from default bookmark
- `DELETE /bookmarks/{bookmarkId}/{itemId}`: Remove an item from a specific bookmark

## Other Features

- `GET /sol-price`: Get SOL price
- `GET /check/{address}`: Check an address
- `GET /vanity/key`: Get vanity key
- `GET /vanity/random-mint-public-key`: Get random mint public key
- `GET /metas/current`: Get current metas
- `GET /metas/search`: Search metas
- `GET /notifications`: Get notifications
- `GET /candlesticks/{mint}`: Get candlestick data for a mint
- `GET /global-params/{timestamp}`: Get global parameters
- `POST /balances/index`: Index balances
- `GET /balances/{address}`: Get balance for an address
- `POST /send-transaction`: Send a transaction
- `POST /send-transaction/check-signatures`: Check transaction signatures
- `GET /send-transaction/jito-tip-account`: Get Jito tip account
- `GET /timeline/{userId}`: Get user timeline
- `POST /feed/add-click/{feedId}`: Add a click to a feed
- `POST /feed/add-load/{feedId}`: Add a load to a feed
- `POST /captcha-score`: Submit captcha score
- `GET /pinata-health/health`: Check Pinata health
- `GET /pinata-health/upload-health`: Check Pinata upload health
- `GET /pinata-health/download-health`: Check Pinata download health
- `GET /era`: Get current era
- `GET /eras`: Get all eras
- `GET /meet`: Get meet information
- `POST /meet/dismiss`: Dismiss meet
- `POST /meet/copy-email`: Copy meet email
- `GET /videos/get-signed-url`: Get signed URL for video
- `GET /videos/get-previews`: Get video previews
- `GET /token/generateTokenForThread`: Generate token for thread
- `POST /ipfs/token-metadata`: Upload token metadata to IPFS
- `POST /ipfs/image`: Upload image to IPFS
- `GET /health`: Check API health

## Data Transfer Objects (DTOs)

The API uses various data transfer objects (DTOs) for different operations. Some of the key DTOs include:

- LoginDto
- ReplyDto
- GetRepliesForMintsDto
- ReplyExperimentalDTO
- BalancesIndexDto
- LivestreamDto
- CreateReportDto
- CreateCommentReportDto
- SeenCoinsDto
- SeenAdvancedCoinsDto
- UploadMetadataDto
- CreateBookmarkDto
- AddOrRemoveItemFromMultipleBookmarksDto
- AddItemToBookmarkDto

For more detailed information about the request and response formats for each endpoint, please refer to the specs
