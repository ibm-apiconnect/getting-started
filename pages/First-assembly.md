---
title: Creating your first assembly
keywords:
tags:
sidebar: 
permalink: /First-assembly.html
summary:
---

Follow these steps:

1. Create API
{% include image.html file="Add-a-new-API.png" max-width="400" alt="Add a new API" %}
{% include image.html file="Add-a-new-API-2.png" max-width="400" alt="Add a new API - step 2" %}
   - Define Swagger definition (don't need Product at this point)
   - Define path
   {% include image.html file="Assembly-editor-paths.png" max-width="600" alt="Edit paths" %}
   - What this does: Creates client ID policy, creates invoke policy
1. Wire up proxy
   - Edit host and path API properties.
   - Path
   - Parameters
   - Response defn.
1. Run using test tool
   - Select product
   - Select catalog and test app
   - Select operation and params
   - Expand debug pane
1. `curl` the new endpoint.  
