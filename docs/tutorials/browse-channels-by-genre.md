---
# markdownlint-disable
# vale  off
layout: default
nav_order: 1
parent: Tutorials
# tags used by AI files
description: Find `channel` resources by genre
tags:
    - api
categories: 
    - tutorial
ai_relevance: high
importance: 6
prerequisites:
    - /before-you-start-a-tutorial
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

# Tutorial: Find all channels in a specific genre

In this tutorial, you'll learn how to use the `genrePop` query parameter to filter channels by their genre.

**Time to complete**: 10-15 minutes

## What you'll achieve

- Find all channels in a specific genre in SiriusXM in the Channels resource.
- Get more information about the request format and required fields
- Verify that your task was successfully created
- Learn how to handle common errors

## Before you start

Make sure you've completed the [Before you start a tutorial](../before-you-start-a-tutorial.md)
topic on the development system you'll use for this tutorial.

### Prerequisites

- Local service is accessible at your configured `base_url`
- Postman app installed

### Using Postman

1. Start the local service if it's not already running:

    ```shell
    cd <your-github-workspace>/tune-guide-api/api
    json-server -w tune-guide-db.json
    ```

2. Open the Postman app on your desktop.
3. Create a new request with these values:
    - **METHOD**: `GET`
    - **URL**: `http://localhost:3000/channels?genre=Pop`
    - **Headers**:
      - `Content-Type: application/json`

4. Click the **Params** tab below the URL field
5. Add a query parameter:
    - **Key:** `genre`
    - **Value:** `Pop`
  
The query parameter filters the results by appending `?genre=Pop` to the URL. Replace `value`
with the genre you want to find. Postman automatically formats the URL with your query parameter.

6. In the Postman app, choose **Send** to make the request.
7. The system returns only genres whose name exactly matches "Pop." The match is case-sensitive
and must be exact. For example, "Pop" won't match "pop."

    ```json
    {
      "channel_number": 2,
      "name": "Hits 1",
      "genre": "Pop",
      "description": "Pop hits, now to next",
      "target_audience": "Gen X, Millennials, Gen Z, Gen alpha",
      "id": 4
    }
    ```

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language.
To do this, adapt the values from the tutorial to the properties
and arguments that the language uses to make REST API calls.

## Verify your genre

Confirm that the service saved your genre correctly by retrieving
it using a `GET` request with the same URL and the `id` from your
response `{base_url}/channels/4`. The response should include the
same genre details you submitted.

## Troubleshooting common errors

|Status Code|Error|Solution|
|---------------------------|------------------------|------------------------------|
|`400 Bad Request`|Missing required field|Ensure request includes all required fields|
|`404 Not Found`|Invalid `id`| Verify channel exists, call `GET /channels`|
|`500 Internal Server Error`|Service connection issue|Check json-server is running|
|`Connection refused`|Service not running|Start local service using step 1|

## Next steps

- Review the [channels api reference](../api/channels.md) for more details.

## Related topics

- [Get all channels](../api/channels-get-all-channels.md) in the system.
- [Get a channel by id](../api/channels-get-channel-by-id.md) in the system.
