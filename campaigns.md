---
layout: default
title: Campaigns
---

## Tasks

Tasks are the internal name for campaigns. Brands create tasks (campaigns) for producers to fulfill.


### Create Task

    DESCRIPTION: creates a task
    METHOD: POST
    URL: /v2/client/hilite/task/direct
    PARAMS:
      - TODO

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
