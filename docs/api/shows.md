---
# markdownlint-disable
# vale  off
layout: default
nav_order: 5
has_children: true
has_toc: false
# tags used by AI files
description: "Information about the `shows` resource"
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
    - /shows
version: "v1.0"
last_updated: "2025-09-03"
# vale  on
# markdownlint-enable
---

# `shows` resource

Base endpoint:

```shell

{server_url}/shows
```

Contains information about the shows of the service.

A show resource describes the shows provided in the service.

## Resource properties

Sample `shows` resource

```js

{
    "show_name": "80s on 8 with Alan Hunter",
    "host": "Alan Hunter",
    "air_time_PDT": "04:00",
    "day_of_week": "Monday, Tuesday, Wednesday, Thursday, Friday",
    "duration_mins": 360,
    "channel_number": 8,
    "id": 1
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `show_name` | string | The name of the show |
| `host` | string | The show's host |
| `air_time_PDT` | number | The time of day the show airs |
| `day_of_week` | string | The days of the week the show airs |
| `duration_mins` | number | How long the show airs for in minutes |
| `channel_number` | number | The Siriux XM channel the show airs on |
| `id` | string | The show's unique ID |

## Read operations

* [Get all shows](shows-get-all-users.md)
* [Get show by ID](shows-get-user-by-id.md)
