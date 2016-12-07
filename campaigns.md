---
layout: default
title: Campaigns
---

## Campaigns

Brands generate campaigns. This is usually done via our [admin console](https://admin.hilite.media) but, if you prefer to build your own, the routes to do so are listed below. Campaigns both send requests to users, and contain all submitted [deliverables](/deliverables.html) for that campaign.

[//]: # (----------------------------------------------------------------------------------------------------------------------------------------)

### Create Campaign
    
**Description**: Creates a new campaign 

**Method**: `POST`

**URL**: `/v1/campaigns?token=<TOKEN>`

**Params**    
      
`uid :: string (required)` name of the campaign (ex. _"Super Bowl Victory Dance"_)
`teleprompter :: string (required)` the text you wish to present to your users (ex. _"Show us your best victory dance!"_)

**Example of a successful response**
        
    {
      "responseCode": 200,
      "data": {
        "campaign": {
          "assetProfile": {},
          "uid": "someuniqueid",
          "teleprompter": "test teleprompter",
          "organizationId": "584750c589b67e0700048cc9",
          "status": "curated - approved",
          "createdAt": "2016-12-06T23:59:02.127Z",
          "updatedAt": "2016-12-06T23:59:02.127Z",
          "id": "584750c689b67e0700048cd3",
          "organization": {
            "name": "My Organization Name",            
            "createdAt": "2016-12-06T23:59:01.430Z",
            "updatedAt": "2016-12-06T23:59:01.430Z",
            "id": "584750c589b67e0700048cc9"
          }
        }
      }
    }    

[//]: # (----------------------------------------------------------------------------------------------------------------------------------------)

### Find All

**Description**: Returns all campaigns for your organization. 

**Method**: `GET`

**URL**: `/v1/campaigns?token=<TOKEN>`

**Example of a successful response**

    {
      "responseCode": 200,
      "data": {
        "campaigns": [
          {
            "assetProfile": {},
            "uid": "Campaign Name 1",
            "teleprompter": "testing one",
            "organizationId": "584753543748bc080054275d",
            "status": "curated - approved",
            "createdAt": "2016-12-07T00:09:56.903Z",
            "updatedAt": "2016-12-07T00:09:56.903Z",
            "id": "584753543748bc0800542762",
            "organization": {
              "name": "My Organization Name",          
              "createdAt": "2016-12-07T00:09:56.361Z",
              "updatedAt": "2016-12-07T00:09:56.361Z",
              "id": "584753543748bc080054275d"
            }
          },
          {
            "assetProfile": {},
            "uid": "Campaign Name 2",
            "teleprompter": "testing two",
            "organizationId": "584753543748bc080054275d",
            "status": "curated - approved",
            "createdAt": "2016-12-07T00:09:56.906Z",
            "updatedAt": "2016-12-07T00:09:56.907Z",
            "id": "584753543748bc0800542763",
            "organization": {
              "name": "My Organization Name",          
              "createdAt": "2016-12-07T00:09:56.361Z",
              "updatedAt": "2016-12-07T00:09:56.361Z",
              "id": "584753543748bc080054275d"
            }
          },
          {
            "assetProfile": {},
            "uid": "Campaign Name 3",
            "teleprompter": "testing three",
            "organizationId": "584753543748bc080054275d",
            "status": "curated - approved",
            "createdAt": "2016-12-07T00:09:56.909Z",
            "updatedAt": "2016-12-07T00:09:56.909Z",
            "id": "584753543748bc0800542764",
            "organization": {
              "name": "My Organization Name",          
              "createdAt": "2016-12-07T00:09:56.361Z",
              "updatedAt": "2016-12-07T00:09:56.361Z",
              "id": "584753543748bc080054275d"
            }
          }
        ]
      }
    }    

[//]: # (----------------------------------------------------------------------------------------------------------------------------------------)

### Find One

**Description**: Find one campaign by its ID 

**Method**: `GET`

**URL**: `/v1/campaigns/:id?token=<TOKEN>` 

**Example of a successful response**

    {
      "responseCode": 200,
      "data": {
        "campaign": {
          "assetProfile": {},
          "uid": "My Campaign Name",
          "teleprompter": "This is some teleprompter text",
          "organizationId": "5848523a9e330308008dc295",
          "status": "curated-approved",
          "createdAt":"2016-12-06T23:59:02.127Z",
          "updatedAt":"2016-12-06T23:59:02.127Z",
          "id":"5848523b9e330308008dc298",
          "organization":{
            "name":"My Organization Name",
            "createdAt":"2016-12-06T23:59:02.127Z",
            "updatedAt":"2016-12-06T23:59:02.127Z",
            "id":"5848523a9e330308008dc295"
          }
        }
      }
    }

[//]: # (----------------------------------------------------------------------------------------------------------------------------------------)

### Update

**Description**: Update a campaign

**Method**: `PUT`

**Params**

`uid :: string` name of the campaign (ex. _"Super Bowl Victory Dance"_)

`teleprompter :: string` the text you wish to present to your users (ex. _"Show us your best victory dance!"_)

`preRoll :: string` Append a video pre roll to uploaded [deliverables](/deliverables.html). Must be a valid asset id and in a valid file format (currently video/mp4, video/quicktime, video/mov, video/ogg). See our [assets](/assets.html) section for more information on how to create an asset.

`postRoll :: string` Append a video post roll to uploaded [deliverables](/deliverables.html). Must be a valid asset id and in a valid file format (currently video/mp4, video/quicktime, video/mov, video/ogg). See our [assets](/assets.html) section for more information on how to create an asset.

**Example of a successful response**

    {
      "responseCode": 200,
      "data": {
        "campaign": {
          "assetProfile": {},
          "uid": "My Campaign Name",
          "teleprompter": "This is some teleprompter text",
          "organizationId": "5848523a9e330308008dc295",
          "status": "curated-approved",
          "createdAt":"2016-12-06T23:59:02.127Z",
          "updatedAt":"2016-12-06T23:59:02.127Z",
          "id":"5848523b9e330308008dc298",
          "organization":{
            "name":"My Organization Name",
            "isRemoved":false,
            "createdAt":"2016-12-06T23:59:02.127Z",
            "updatedAt":"2016-12-06T23:59:02.127Z",
            "id":"5848523a9e330308008dc295"
          }
        }
      }
    }


[//]: # (----------------------------------------------------------------------------------------------------------------------------------------)

### Delete

**Description**: Delete a campaign by its ID 

**Method**: `DELETE`

**URL**: `/v1/campaigns?token=<TOKEN>`

**Example of a successful response**

    {
      "responseCode": 200,
      "data": {
        "campaign": {
          "assetProfile": {},
          "uid": "someuniqueid",
          "teleprompter": "test teleprompter",
          "organizationId": "584750c589b67e0700048cc9",
          "status": "curated - approved",
          "createdAt": "2016-12-06T23:59:02.127Z",
          "updatedAt": "2016-12-06T23:59:02.127Z",
          "id": "584750c689b67e0700048cd3",
          "organization": {
            "name": "My Organization Name",            
            "createdAt": "2016-12-06T23:59:01.430Z",
            "updatedAt": "2016-12-06T23:59:01.430Z",
            "id": "584750c589b67e0700048cc9"
          }
        }
      }
    }

[//]: # ( TODO:  destroyPreRoll, and destroyPostRoll)