---
layout: default
title: Webhooks
category: endpoint
---

## Webhooks

Webhooks allow external services to be notified when certain events happen within the HILITE system that affect your organization (example: a new video gets uploaded for a campaign). When the specified events happen, we’ll send a POST request to each of the URLs you provide.

We provide an interface to define these in our [admin console](https://admin.hilite.media) but, if you prefer to build your own the routes to do so are listed below. 

{% include endpoint.html endpoints=site.data.endpoints.webhooks %}