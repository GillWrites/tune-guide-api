---
# markdownlint-disable
# vale  off
layout: default
parent: channels resource
nav_order: 1
# tags used by AI files
description: GET all `channels` resources from the service
tags:
    - api
categories:
    - api-reference
ai_relevance: high
importance: 7
prerequisites:
    - /api/channels
related_pages: []
examples: []
api_endpoints: 
    - GET /channels
version: "v1.0"
last_updated: "2025-09-03"
# vale  on
# markdownlint-enable
---

# Get all channels

Returns an array of [`channel`](channels.md) objects that contains all channels provided by the service.

## URL

```shell

{server_url}/channels
```

## Parameters

None

## Request headers

None

## Request body

None

## Return body

```js
[
   {
      "channel_number": 8,
      "name": "80s on 8",
      "genre": "1980s",
      "description": "Pop hits from the 1980s MTV era",
      "target_audience": "Baby boomers, Gen X, Millennials",
      "id": 1
    },
    {
      "channel_number": 34,
      "name": "Lithium",
      "genre": "Grunge rock, 90s alternative",
      "description": "Grunge and 90s alternative rock",
      "target_audience": "Grunge fans, 90s rock fans, Gen X, Millennials",
      "id": 2
    },
    {
      "channel_number": 26,
      "name": "Classic Vinyl",
      "genre": "1960s, 1970s",
      "description": "60s/70s classic rock",
      "target_audience": "Baby boomers, Gen X, Millennials",
      "id": 3
    },
    {
      "channel_number": 2,
      "name": "Hits 1",
      "genre": "Pop",
      "description": "Pop hits, now to next",
      "target_audience": "Gen X, Millennials, Gen Z, Gen alpha",
      "id": 4
    }
    ...
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
