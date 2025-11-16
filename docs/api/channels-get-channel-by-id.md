---
# markdownlint-disable
# vale  off
layout: default
parent: channels resource
nav_order: 2
# tags used by AI files
description: GET the `channels` resource with the specified ID from the service
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

# Get a channel by ID

Returns an array of  [`channel`](channels.md) objects that contains only the channel specified by the `id` parameter, if it exists.

## URL

```shell

{server_url}/channels/{id}
```

## Parameters

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | The record ID of the channel to return |

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
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
