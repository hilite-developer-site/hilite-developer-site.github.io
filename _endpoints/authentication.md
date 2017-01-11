---
layout: default
title: Authentication
category: endpoint
---

## Authenticating a request

All consumers of the HILITE api must be assigned a user account from the betacamp team. We plan to automate this process in the future via a developer console. Upon account creation a user is issued an api token. *All requests must include this token*. The expected format is `https://api.hilite.media/v2/route?token=<TOKEN>`. At present there is no expiration date on this token but it can be revoked by the betacamp team at any time.

{% include endpoint.html endpoints=site.data.endpoints.authentication %}