---
# markdownlint-disable
# vale  off
layout: default
nav_order: 5
has_children: true
has_toc: false
# tags used by AI files
description: "Information about the `channels` resource"
tags: 
    - api
categories:
    - api-reference
ai_relevance: high
importance: 8
prerequisites: []
related_pages: 
    - /tutorials/before-you-start-a-tutorial
examples: []
api_endpoints: 
    - /channels
version: "v1.0"
last_updated: "2025-09-03"
# vale  on
# markdownlint-enable
---

# `channels` resource

Base endpoint:

```shell

{server_url}/channels
```

Contains information about the channels of the service.

## Resource properties

Sample `channel` resource

```js

{
    "channel_number": 8,
      "name": "80s on 8",
      "genre": "1980s",
      "description": "Pop hits from the 1980s MTV era",
      "target_audience": "Baby boomers, Gen X, Millennials",
      "id": 1
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `name` | string | The channel name |
| `genre` | string | The type of music played on the channel |
| `description` | string | Tagline about the channel |
| `target_audience` | string | The channel's targeted demographic |
| `id` | number | The channels's unique record ID |

## Read operations

* [Get all channels](channels-get-all-channels.md)
* [Get channels by ID](channels-get-channel-by-id.md)
