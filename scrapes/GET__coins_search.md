# GET /coins/search

## Description
Search for coins based on a query term with filtering, sorting, and pagination.

## Base URL
`https://frontend-api-v3.pump.fun`

## Query Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `limit` | number | Yes | No description available |
| `offset` | number | Yes | No description available |
| `sort` | string | Yes | No description available |
| `searchTerm` | string | Yes | No description available |
| `order` | string | Yes | No description available |
| `includeNsfw` | boolean | Yes | No description available |
| `creator` | string | Yes | No description available |
| `complete` | boolean | Yes | No description available |
| `meta` | string | Yes | No description available |
| `type` | string | Yes | No description available |

## Headers
| Header | Value | Required |
|--------|-------|----------|
| `Authorization` | `Bearer <JWT>` | Yes |

### Example Request
```bash
curl -X GET "https://frontend-api-v3.pump.fun/coins/search" \
  -H "Authorization: Bearer YOUR_JWT_TOKEN"
```

## Response Examples

### Example 1
**Status:** `200`

**Parameters:**
```json
{
  "limit": 10,
  "offset": 0,
  "sort": "market_cap",
  "searchTerm": "",
  "order": "ASC",
  "includeNsfw": true,
  "creator": "",
  "complete": true,
  "meta": "",
  "type": ""
}
```

**Response Data:**
```json
{
  "0": {
    "mint": "C2QPnV51mF5juU6AXtdZgYKk8kWPNrPa1qAipB2vXa67",
    "name": "widecat",
    "symbol": "WIDECAT",
    "description": "the cat is wide  https://t.me/widecatcoin https://twitter.com/widecatcoin https://www.widecat.xyz/",
    "image_uri": "https://cf-ipfs.com/ipfs/QmZeWReJb3wXYj9jRx8uHkeqC5Uth8mu8jYJv7nsZWpCyi",
    "metadata_uri": "https://cf-ipfs.com/ipfs/QmUwQT8rWQXVyytH2AgzfozeRa5UM9vq4dkxBC2EiSe8K5",
    "twitter": "https://twitter.com/widecatcoin",
    "telegram": "https://t.me/widecatcoin",
    "bonding_curve": "8QizEw5hvsmDjYyf8jvefPpWp6Fei2qJSbtKBCKeZR6c",
    "associated_bonding_curve": "CpSYLkJxNzeUtgvccfRsaMAwHuhyn2uMRcEWoBVyKTmH",
    "creator": "2oLLMdw95kvTej3m4xG3cQjjj2HPyWKSmvU5EnJ7gS82",
    "created_timestamp": 1712798083000,
    "raydium_pool": "68NwtzbHRDoBKsRXygUYzX7xT1F2EruEp4XSiGQ6tFPR",
    "complete": true,
    "virtual_sol_reserves": 115005359393,
    "virtual_token_reserves": 279900000000000,
    "total_supply": 1000000000000000,
    "website": "https://www.widecat.xyz/",
    "show_name": true,
    "king_of_the_hill_timestamp": 1712798740071,
    "market_cap": 14.790000000000001,
    "reply_count": 62,
    "last_reply": 1732935085862,
    "nsfw": false,
    "market_id": "4uqWddbVXqcFc3iPs9GXvYLW7HXngbFkshWo3EiPX4Hg",
    "banner_uri": null,
    "video_uri": null,
    "is_banned": false,
    "program": null,
    "usd_market_cap": 3611.718,
    "is_currently_live": false
  },
  "1": {
    "mint": "6ULTsikCoXVTBtB23gNhgk4eD2RMRGsQre5PZKiLpump",
    "name": "Good Boi",
    "symbol": "GB",
    "description": null,
    "image_uri": "https://ipfs.io/ipfs/QmUQB3v69ouXjJCJvrp8o4JA5KQKjE1yptcLBC5D3Dfokw",
    "metadata_uri": "https://ipfs.io/ipfs/QmQ6BfNEE3fxk2Fuo4CF19qPvTZtJ9tVKV4Krp197dfb47",
    "twitter": null,
    "telegram": null,
    "bonding_curve": "EMoX7waWBtRotGLzQ2JE6eCBWLXiXrzL43s45UXU6Wcr",
    "associated_bonding_curve": "FcWv8FwY22AC4kvaRishKuEHkMiHhLcUXAzt1ZuABAGG",
    "creator": "5tYLQBEtHcEeAN9i9XGovu4B4uYdY4AhQZgp8YiMxCzS",
    "created_timestamp": 1731900921581,
    "raydium_pool": "7vbLRZKiEHgU1bKw6PxtP6j17okqhHD8Y5dhBHhn6Kzb",
    "complete": true,
    "virtual_sol_reserves": 115005359226,
    "virtual_token_reserves": 279900000000000,
    "total_supply": 1000000000000000,
    "website": null,
    "show_name": true,
    "king_of_the_hill_timestamp": 1731901046000,
    "market_cap": 14.75,
    "reply_count": 21,
    "last_reply": 1731902174008,
    "nsfw": false,
    "market_id": "3XBiqckE75qQFAn55atxUjJDymAgL6aVpTfmKK8KsctD",
    "banner_uri": null,
    "video_uri": null,
    "is_banned": false,
    "program": null,
    "usd_market_cap": 3601.95,
    "is_currently_live": false
  },
  "2": {
    "mint": "6K9BMkw1jFtegiHzpCrVPxAwJvSuCq2VXrmgxFVypump",
    "name": "The Cold Side of the Pillow",
    "symbol": "cold",
    "description": "dat shit bussin frfr",
    "image_uri": "https://cf-ipfs.com/ipfs/QmVJSoKax2krbPV3PNd5BUL8ejdN6RZwsXKQet5KBJYxDh",
    "metadata_uri": "https://cf-ipfs.com/ipfs/QmazvRg2Td1YnajbNVX9zCEdLHhv9WPCyuJHawiHJknJV8",
    "twitter": "https://x.com/coldpillowsol",
    "telegram": "https://t.me/TheColdSideofthePillowSol",
    "bonding_curve": "5edLG1pSSrN1jZ6Y8CC3FtRfEwSVh8jzuVjeb5sRvrvb",
    "associated_bonding_curve": "4kymxTF243wHBoBB5uowYnoAYHLoEGXb7et4q23FDgCc",
    "creator": "EL66BEzDARscyhRVkmZdURvmDEx5bwSFUicWNXC83Jxf",
    "created_timestamp": 1721847490234,
    "raydium_pool": "CwcBowLParyGq1vBVwLgAq4QgZnCFhoUSUmh9Lgof7Bm",
    "complete": true,
    "virtual_sol_reserves": 115005359632,
    "virtual_token_reserves": 279900000000000,
    "total_supply": 1000000000000000,
    "website": "https://thecoldsideofthepillow.xyz/",
    "show_name": true,
    "king_of_the_hill_timestamp": 1721848264000,
    "market_cap": 14.219999999999999,
    "reply_count": 34,
    "last_reply": 1721849648192,
    "nsfw": false,
    "market_id": "7NDh77kCwmLUS12aEgoqx7ZybZdxyRoLKZaSBXbrsfRF",
    "banner_uri": null,
    "video_uri": null,
    "is_banned": false,
    "program": null,
    "usd_market_cap": 3472.5239999999994,
    "is_currently_live": false
  },
  "3": {
    "mint": "5ATM8uCML3gc33njabRix7VNLyoW5Rb27GS6j9zspump",
    "name": "DUNA ",
    "symbol": "DUNA ",
    "description": "decentralized unincorporated nonprofit association: legal dao formation in wyoming",
    "image_uri": "https://ipfs.io/ipfs/QmeKUxLSzbEjCeXpiVqjRYX6dEeWEUgsNohgUozUTkGxyc",
    "metadata_uri": "https://ipfs.io/ipfs/QmTrSMYhMMyXGEi9yR8kxQdtZF8RidaPy2RXQaSYVcE7gW",
    "twitter": "https://x.com/markus9x/status/1861242414515777767",
    "telegram": null,
    "bonding_curve": "9vio8N1PZaJ5p1fijGB2Y6y7V2Qt1heTupPTs2E16tu6",
    "associated_bonding_curve": "sGWY9B61EF7zGW3Dpv1R5YdbE4iqji4gXfkb7ndk7m4",
    "creator": "6Wy5X6csKtWvuWLZBHdL5tekrygfRHTSPMFzCPxj1WrQ",
    "created_timestamp": 1732590409738,
    "raydium_pool": "5qTS1yBSL8WXWYJJFayjYQci6z6p3QzxuQdjDrm4Vw1j",
    "complete": true,
    "virtual_sol_reserves": 115005359178,
    "virtual_token_reserves": 279900000000000,
    "total_supply": 1000000000000000,
    "website": null,
    "show_name": true,
    "king_of_the_hill_timestamp": 1735770138000,
    "market_cap": 13.12,
    "reply_count": 49,
    "last_reply": 1735960233681,
    "nsfw": false,
    "market_id": "5Ddic8sqnZBbYg1Q9dVLB5jfLX8rXuJCFsXqYN7fUFxw",
    "banner_uri": null,
    "video_uri": null,
    "is_banned": false,
    "program": null,
    "usd_market_cap": 3203.9039999999995,
    "is_currently_live": false
  },
  "4": {
    "mint": "FVCaZidfNN6Ut1WBtaTKfsowDpjWVhc7o399RGNaaXtZ",
    "name": "OPTIMUS CAT",
    "symbol": "OPTICAT",
    "description": null,
    "image_uri": "https://ipfs.io/ipfs/QmcMsBeQkLkQR9hU8k6jaRHNo1Y9zzm7HoNPVSJDb6nwFr",
    "metadata_uri": "https://ipfs.io/ipfs/QmWCTs8BUUjsigmSTneM21USbbUqE5kDn2XeM7BFJ3MwM7",
    "twitter": null,
    "telegram": null,
    "bonding_curve": "3AzEqi56xt5deTScyhy42mLeajEafoT9GUBc9E9SThqJ",
    "associated_bonding_curve": "9urmFCFyBNXoeVEzetx84HiE8k7eX3FBh1jXzEzd9NXo",
    "creator": "4KJ9Eu8JRS8wqH7PJT4rgyvFdL88kKUj91R76wx5jxD9",
    "created_timestamp": 1731995136230,
    "raydium_pool": "3AMgNWW15eZb2Fx7kGqscmBKqNuyrNABR6tQnVfDNZtK",
    "complete": true,
    "virtual_sol_reserves": 115005359315,
    "virtual_token_reserves": 279900000000000,
    "total_supply": 1000000000000000,
    "website": null,
    "show_name": true,
    "king_of_the_hill_timestamp": 1731995139000,
    "market_cap": 13.049999999999999,
    "reply_count": 6,
    "last_reply": 1731995464733,
    "nsfw": false,
    "market_id": "GNr6ECW2yPUjHhHSjaEPk2g5b1vTojohhkWCxJSgLhQH",
    "banner_uri": null,
    "video_uri": null,
    "is_banned": false,
    "program": null,
    "usd_market_cap": 3186.8099999999995,
    "is_currently_live": false
  },
  "5": {
    "mint": "AyqDG7u1Z2JbuaiUzdtwDKdaaXy3W3BHUXgR5QbFpump",
    "name": "Ascii Doge",
    "symbol": "Ascii Doge",
    "description": null,
    "image_uri": "https://ipfs.io/ipfs/QmVKL9hn8srRwSdrpv3bH3qc2PwbVGLsCRZTccSqKwNNqz",
    "metadata_uri": "https://ipfs.io/ipfs/QmQEGQArqv8UJZn2hyZfHWCD5SQwSTc1Y2g6o3zmErXeJV",
    "twitter": "https://x.com/dogecoin/status/1858719324078567670",
    "telegram": "https://x.com/dogecoin/status/1858719324078567670",
    "bonding_curve": "4vH9fc9hAFxVZRdfDoqFfkkrXSmTEuY3T8TAp2yiDKTY",
    "associated_bonding_curve": "BX6qDX1ryyML1qCXQwDaU5AnmmnL7bEBh6g1N7HkXeFW",
    "creator": "D1tckBKfmeyxxRgmbMwfhGB13tPp9wKyV23RxYKXa8Ud",
    "created_timestamp": 1731988415778,
    "raydium_pool": "4N6mWmpq4mKbfV2rAnVyipbzTndash9QTMpgpR2Kd1hA",
    "complete": true,
    "virtual_sol_reserves": 115005359067,
    "virtual_token_reserves": 279900000000000,
    "total_supply": 1000000000000000,
    "website": "https://x.com/dogecoin/status/1858719324078567670",
    "show_name": true,
    "king_of_the_hill_timestamp": 1731988418000,
    "market_cap": 12.72,
    "reply_count": 28,
    "last_reply": 1737150685000,
    "nsfw": false,
    "market_id": "Eq4UXQ595gyvvJ2RcTcXyo33gcRFudjifmu3Azpz8eZd",
    "banner_uri": null,
    "video_uri": null,
    "is_banned": false,
    "program": null,
    "usd_market_cap": 3106.224,
    "is_currently_live": false
  },
  "6": {
    "mint": "AR5dRGmPKUKFUFZCuGpMUiKm86oHPzzWJRFBqfQsXnzz",
    "name": "SINTX",
    "symbol": "SINTX",
    "description": "SINTX Technologies, Inc. but on fucking SOL. LETS RUN IT. Bio BS - Engages in the development and commercialization of silicon nitride for medical and non-medical applications. It markets spinal fusion products and develops products for use in total hip and knee joint replacements. The company was founded by Aaron A. Hofmann and Ashok C. Khandkar in 1996 and is headquartered in Salt Lake City, UT. The listed name for SINT is SiNtx Technologies, Inc. Common Stock. ",
    "image_uri": "https://cf-ipfs.com/ipfs/Qmefz2vtVT1dkED1fSGHMDXbtUqVPBHV25x24SmxV1sAmt",
    "metadata_uri": "https://cf-ipfs.com/ipfs/QmY5BmJBiJY4DfbDM1d13dckGGzhBvkjWpvAqjQywPLVup",
    "twitter": "https://twitter.com/SINTXTechnolog1",
    "telegram": null,
    "bonding_curve": "DrcRh7c4948V5sb2zs9BpCNucfU1N5tnmMRd3AG1oZRw",
    "associated_bonding_curve": "DJZ1qBjzSi7AgAfe2i6G2WJ9mctfhcAVa2iSz18rrjR4",
    "creator": "DVN7E8MsjV8kELFH2ALXjFLzKtDCaFA6dXBLzmicbGyo",
    "created_timestamp": 1715772734379,
    "raydium_pool": "C4CEKoFD88pyFCRKL5YeRtDUsAeYRU4H52MpJTJKtBRa",
    "complete": true,
    "virtual_sol_reserves": 115005359524,
    "virtual_token_reserves": 279900000000000,
    "total_supply": 1000000000000000,
    "website": "https://sintx.com/",
    "show_name": true,
    "king_of_the_hill_timestamp": 1715782399592,
    "market_cap": 12.520000000000001,
    "reply_count": 33,
    "last_reply": 1731161559296,
    "nsfw": false,
    "market_id": "Hgvk6gKaAX6Dj6iCfjghuWcY3bvYZTW7Rmx2RCFy7kUc",
    "banner_uri": null,
    "video_uri": null,
    "is_banned": false,
    "program": null,
    "usd_market_cap": 3057.384,
    "is_currently_live": false
  },
  "7": {
    "mint": "7hz17Bed3PFBdfAHqwUXW6TYjHQCHGxchpo6ay2a27pR",
    "name": "PedoExpress",
    "symbol": "PedExpress",
    "description": "The best-selling Christmas movie is now available on Solana! || Starring P. Diddy, Jeffrey Epstein, and Harvey Weinstein",
    "image_uri": "https://cf-ipfs.com/ipfs/Qma62N8epNCkDtwr6CuHUqqkGjio1onGp67gTAGJ5rHTtg",
    "metadata_uri": "https://cf-ipfs.com/ipfs/QmPjA3vj1tUTxMMtN5tDbVwKcLvzNG1v7N4qRuVyu3bWqG",
    "twitter": "twitter.com/pedoexpresssol",
    "telegram": "https://t.me/+h_Dt3Tia3fphNGVk",
    "bonding_curve": "2J3kqips5HWUrpF5nSQDSyGt4DakS7K4aHXFFSJPJsxp",
    "associated_bonding_curve": "2FgQDngEANLj5YgNyWTuiyGnzRfmpRXa6Cw96d1rnihz",
    "creator": "4c5QhJg6LJevjLD4Tz37YTykazWFqa93vx8E5JDUapaM",
    "created_timestamp": 1715812802880,
    "raydium_pool": "9nQCgaZz8KkbB1QEXkjmEecFVSn1rPmojqXpgPY4pXtf",
    "complete": true,
    "virtual_sol_reserves": 115005361449,
    "virtual_token_reserves": 279900000000000,
    "total_supply": 1000000000000000,
    "website": "https://pedexpress.top/",
    "show_name": true,
    "king_of_the_hill_timestamp": 1715874693441,
    "market_cap": 11.41,
    "reply_count": 36,
    "last_reply": 1744651445000,
    "nsfw": false,
    "market_id": "N37gdnCt87RTzomgiVnYfG6UngpxuC2fdNPLoHx7e1C",
    "banner_uri": null,
    "video_uri": null,
    "is_banned": false,
    "program": null,
    "usd_market_cap": 2786.322,
    "is_currently_live": false
  },
  "8": {
    "mint": "9vjfTxDhkEscap1h2Cahmb79vPzcDwK9UHLADdeJpump",
    "name": "Doge pilled",
    "symbol": "Dp",
    "description": null,
    "image_uri": "https://ipfs.io/ipfs/QmWVMAp6yxYy7MGU63TzMtR5FgrqTHQZUPazCRkSfoC2E1",
    "metadata_uri": "https://ipfs.io/ipfs/QmPbptaRRRHa6P24UkwWqnGXsWRL9CoGqcZ5M8Vec19CRB",
    "twitter": null,
    "telegram": null,
    "bonding_curve": "GP1txwzC8qGm1hLb3oGT99cMrPFX6FPVQ1Zq8qFWJZYs",
    "associated_bonding_curve": "ATkQAoiPcjNcFBDSj7KderzLUmojGmfkLhjoh6y2PrQi",
    "creator": "5VCKq3iZUy4waZ7bUmGU76CUg7bpgzmbEinTNh51MXtB",
    "created_timestamp": 1731997532559,
    "raydium_pool": "4Ss2hqT549vDniREn5YsxBHgj3f8zSph8Zgfh9E2JfQi",
    "complete": true,
    "virtual_sol_reserves": 115005359145,
    "virtual_token_reserves": 279900000000000,
    "total_supply": 1000000000000000,
    "website": null,
    "show_name": true,
    "king_of_the_hill_timestamp": 1731997565000,
    "market_cap": 9.869,
    "reply_count": 14,
    "last_reply": 1737150615000,
    "nsfw": false,
    "market_id": "AEaWn67oEqyA1nRrCauSLKvdnmxUFSKQBJypX8Y51o2S",
    "banner_uri": null,
    "video_uri": null,
    "is_banned": false,
    "program": null,
    "usd_market_cap": 2410.0098,
    "is_currently_live": false
  },
  "9": {
    "mint": "yy29xhRNBWFrt9KcHQeG5FjTV2M8jYy7hZsqtxYpump",
    "name": "PumpFlow AI",
    "symbol": "⎊",
    "description": "We are the market leader in solana token-pair evaluation. Enabling users to get a cutting edge on the crypto market. $⎊",
    "image_uri": "https://ipfs.io/ipfs/QmS9aV3Uorj8yRwsxqYhAtfJwTEBpgW2rHxcWos7TiZjtJ",
    "metadata_uri": "https://ipfs.io/ipfs/QmeqjqYMr1nEEwYhn7f4ewGqMVWPYg2QZZxmyQfMRgGyJ2",
    "twitter": "https://x.com/PumpFlowAI",
    "telegram": null,
    "bonding_curve": "4p4bPzm5498Ni9MAtzNi85U3jhrb6nssSY3g9oa2cPQn",
    "associated_bonding_curve": "5orBXtVLpRkffJyEAaSEkaZvpxeikbpc8gtBRfQ1kXTh",
    "creator": "CsJK9ioQAvaScZkdu41QFRdWRqAQHFMfTZ5MU6r2SbWj",
    "created_timestamp": 1731997676534,
    "raydium_pool": "82XRgmn6r8TzyfczJ3MQPtjDAsv44wwuCA8QTHDRxP5n",
    "complete": true,
    "virtual_sol_reserves": 115005359091,
    "virtual_token_reserves": 279900000000000,
    "total_supply": 1000000000000000,
    "website": "https://www.pumpflowai.xyz/",
    "show_name": true,
    "king_of_the_hill_timestamp": 1731997700000,
    "market_cap": 2.875,
    "reply_count": 38,
    "last_reply": 1752087921000,
    "nsfw": false,
    "market_id": "HjYLMA19GJZh1qxXLgEfYitmBXQiwJFYSUQdA2o3PsEm",
    "banner_uri": null,
    "video_uri": null,
    "is_banned": false,
    "program": null,
    "usd_market_cap": 702.0749999999999,
    "is_currently_live": false
  }
}
```

**Test Summary:**
- Total test cases: 5
- Successful responses: 5
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
