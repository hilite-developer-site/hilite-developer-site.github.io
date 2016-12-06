---
layout: default
title: Campaigns
---

## Campaigns

Brands generate campaigns. This is usually done via our [admin console](https://admin.hilite.media) but, if you prefer to build your own the routes to do so are listed below. Campaigns both send requests to users, and contain all submitted [deliverables](/deliverables.html) for that campaign.


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
      "task": { 
        "assetProfile": {},
        "uid": "someuniqueid",
        "teleprompter": "test teleprompter",
        "organizationId": "5846f3e75f6fd208001a8742",
        "status": "curated - approved",
        "type": "direct",
        "eid": "someeventid",
        "isRemoved": false,
        "isPlayerHidden": false,
        "createdAt": "2016-12-06T17:22:48.335Z",
        "updatedAt": "2016-12-06T17:22:48.335Z",
        "id": "5846f3e85f6fd208001a874c" 
      }       
    }    

### List Tasks

    DESCRIPTION: retrieves all active tasks for an api users organization
    METHOD: GET
    URL: /v2/client/hilite/task/direct
    PARAMS:
      - eid (optional) :: string
        - unique id for an event or other special occasion
      - uid (optional) :: string
        - unique id for a campaign


### Delete Task

    DESCRIPTION: deletes a task by id
    METHOD: DELETE
    URL: /v2/client/hilite/task/:id
