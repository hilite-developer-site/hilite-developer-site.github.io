---
layout: default
title: Assets
---

#Assets

Routes relating to branding assets that organizations can use for UGVC Pre/Post roll etc.

##List assets 
    DESCRIPTION: returns a list of all assets for an organization
    METHOD: GET
    URL: /v2/assets?token=<API TOKEN>      


##Initiate upload
    DESCRIPTION: hands down a signed put URL that is then used for uploading files to S3
    METHOD: POST     
    URL: /v2/assets/initiateUpload


##Complete upload
    DESCRIPTION: post s3 upload, creates an asset record
    METHOD: POST
    URL: /v2/assets/completeUpload


##Delete asset
    DESCRIPTION: removes an asset (non destructively)
    METHOD: 'DELETE
    URL: /v2/assets/:id