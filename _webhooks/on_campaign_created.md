---
layout: default
title: On Campaign Created
display-order: 3
---

### On Video Submitted

**Description**: This hook fires when a new campaign is created. This would be an excellent place to integrate a notification system. See the campaign [specification]({{ "/specs/campaign.html" | prepend: site.baseurl }}) and/or [endpoint]({{ "/endpoints/campaigns.html" | prepend: site.baseurl }}) documentation for more details.

**Payload**: Sends a JSON payload that conforms to the [campaign]({{ "/specs/campaign.html" | prepend: site.baseurl }}) specification. 