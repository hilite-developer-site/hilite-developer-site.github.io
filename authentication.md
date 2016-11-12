---
layout: default
title: Authentication
---

## Authenticating a request

All consumers of the HILITE api must be assigned a user account from the betacamp team. We plan to automate this process in the future via a developer console. Upon account creation a user is given an api token. *All requests must include this token*. The expected format is `https://api.hilite.media/v2/route?token=<TOKEN>`. At present there is no expiration date on this token but it can be revoked by the betacamp team at any time.

`TODO: MIGRATE TOKEN AUTHENTICATION TO AUTHENTICATION HEADER. JWT FORMAT?`

## Token retrieval.

For convenience we have set up login/logout routes to allow retreival of the information an api consumer along with their user profile.

### Login

    DESCRIPTION: get the account details of an existing user account including its API token
    METHOD: POST
    URL: /v1/auth/local
    PARAMS:
      - identifier :: string
      - password   :: string

sample response

    TODO