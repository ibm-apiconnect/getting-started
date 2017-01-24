---
title: Creating your first assembly
layout: tutorial
sidebar: assembly
permalink: /assembly-1.html
summary: An assembly is an application programming interface that calls out to external services and then transforms and aggregates the responses before relaying a response to the calling application.
---
Create API:

{% include image.html file="Add-a-new-API.png" max-width="400" alt="Add a new API" %}
{% include image.html file="Add-a-new-API-2.png" max-width="400" alt="Add a new API - step 2" %}
   - Define Swagger definition (don't need Product at this point)
   - Define path
   {% include image.html file="Assembly-editor-paths.png" max-width="600" alt="Edit paths" %}
   - What this does: Creates client ID policy, creates invoke policy
