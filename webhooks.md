---
layout: default
title: Webhooks
---

Webhooks allow external services to be notified when certain events happen within the HILITE system that affect your organization (example: a new video gets uploaded for a campaign). When the specified events happen, we’ll send a POST request to each of the URLs you provide.

We provide an interface to define these in our [admin console](https://admin.hilite.media) but, if you prefer to build your own the routes to do so are listed below. 

## List available Webhooks 

**Description**: Returns an array of available Webhooks. If one or more have been defined, they will be included. 

**Method**: `GET`

**URL**: `/v1/webhooks?token=<TOKEN>`
      
**Example of a successful response**
        
    {
      "responseCode": 200,
      "data": {
        "webHooks": [
          {
            "displayName": "On Video Submitted",
            "description": "This hook fires when a new video is uploaded to one of your campaigns.",
            "webHookHandle": "ON_VIDEO_SUBMITTED",
            "organizationId": "abcdefghijklmnopqrstuvwxyz",
            "url": https://example.com,
            "id": "abcdefghijklmnopqrstuvwxyz",
            "createdAt": "2016-12-06T06:07:19.999Z",
            "updatedAt": "2016-12-06T06:07:19.999Z"
          },
          {
            "displayName": "On Video Approved",
            "description": "This hook fires when an uploaded video has been approved by a curator.",
            "webHookHandle": "ON_VIDEO_APPROVED",
            "organizationId": null,
            "url": null,
            "id": null,
            "createdAt": null,
            "updatedAt": null
          }
        ]
      }
    }