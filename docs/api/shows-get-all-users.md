---
# markdownlint-disable
# vale  off
layout: default
parent: shows resource
nav_order: 1
# tags used by AI files
description: GET all `shows` resources from the service
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

# Get all shows

Returns an array of [`shows`](shows.md) objects that contains all shows provided by the service.

## URL

```shell

{server_url}/shows
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
      "show_name": "80s on 8 with Alan Hunter",
      "host": "Alan Hunter",
      "air_time_PDT": "04:00",
      "day_of_week": "Monday, Tuesday, Wednesday, Thursday, Friday",
      "duration_mins": 360,
      "channel_number": 8,
      "id": 1
    },
    {
      "show_name": "80s on 8 with Mark Goodman",
      "host": "Mark Goodman",
      "air_time_PDT": "13:00",
      "day_of_week": "Monday, Tuesday, Wednesday, Thursday, Friday",
      "duration_mins": 360,
      "channel_number": 8,
      "id": 2
    },
    {
      "show_name": "Madison On Lithium",
      "host": "Madison",
      "air_time": "03:00",
      "day_of_week": "Monday, Wednesday, Thursday, Friday",
      "duration": 300,
      "channel_number": 34,
      "id": 3
    },
    {
      "show_name": "Kat Corbett On Lithium",
      "host": "Kat Corbett",
      "air_time_PDT": "15:00",
      "day_of_week": "Monday, Tuesday, Thursday, Sunday",
      "duration_mins": 360,
      "channel_number": 34,
      "id": 4
    },
    {
      "show_name": "Classic Vinyl with Earle Bailey",
      "host": "Earle Bailey",
      "air_time_PDT": "14:00",
      "day_of_week": "Monday, Tuesday, Wednesday, Thursday, Friday",
      "duration_mins": 360,
      "channel_number": 26,
      "id": 5
    },
    {
      "show_name": "Classic Vinyl with Rachel Steele",
      "host": "Rachel Steele",
      "air_time_PDT": "08:00",
      "day_of_week": "Monday, Tuesday, Wednesday, Thursday, Friday",
      "duration_mins": 360,
      "channel_number": 26,
      "id": 6
    },
    {
      "id": 7
    },
    {
      "show_name": "One Man Revolution",
      "host": "Tom Morello",
      "air_time_PDT": "10:00",
      "day_of_week": "Friday",
      "duration_mins": 120,
      "channel_number": 34,
      "id": 8
    }
  ]
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
