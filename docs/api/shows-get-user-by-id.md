---
# markdownlint-disable
# vale  off
layout: default
parent: shows resource
nav_order: 2
# tags used by AI files
description: GET the `shows` resource with the specified ID from the service
tags:
    - api
categories:
    - api-reference
ai_relevance: high
importance: 7
prerequisites: 
    - /api/shows
related_pages: []
examples: []
api_endpoints: 
    - GET /shows
version: "v1.0"
last_updated: "2025-09-03"
# vale  on
# markdownlint-enable
---

# Get a show by ID

Returns an array of  [`show`](shows.md) objects that contains only the show specified by the `id` parameter, if it exists.

## URL

```shell

{server_url}/show/{id}
```

## Parameters

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | The record ID of the show to return |

## Request headers

None

## Request body

None

## Return body

```js
[
    {
      "show_name": "80s on 8 with Alan Hunter",
      "host": "Alan Hunter",
      "air_time_PDT": "04:00",
      "day_of_week": "Monday, Tuesday, Wednesday, Thursday, Friday",
      "duration_mins": 360,
      "channel_number": 8,
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
