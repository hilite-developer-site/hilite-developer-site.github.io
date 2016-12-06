---
layout: default
title: Authentication
---

## Authenticating a request

All consumers of the HILITE api must be assigned a user account from the betacamp team. We plan to automate this process in the future via a developer console. Upon account creation a user is issued an api token. *All requests must include this token*. The expected format is `https://api.hilite.media/v2/route?token=<TOKEN>`. At present there is no expiration date on this token but it can be revoked by the betacamp team at any time.

## Token retrieval

**Description**: Returns an authorization token for use in subsequent requests. It is the responsibility of the client to store this token for later retrieval. For web based clients we suggest storing it in a cookie or local storage. 

**Method**: `POST`

**URL**: `/v1/authenticate`

**Parameters**
      
    - identifier :: string (required)
    - password   :: string (required)
      
**Example of a successful response**
        
    {
        responseCode: 200,
        data: {
            token: abcd-efgh-jklm-nopq-rstuv-wxyz
        }
    }