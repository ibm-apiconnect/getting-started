---
title: Building an API proxy
keywords:
tags:
sidebar: gs_sidebar
permalink: proxy.html
summary:
---
### Creating your first Assembly

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

Deploying Assemblies to Bluemix

### Exposing SOAP services as REST APIs

1. Create API defn.
1. Create target service
   - Provide URL of WSDL file
1. Create in the Swagger API defn.
1. Create operation switch
   - Add case for getForecastByZip (operation defined in swagger)
1. Add map for request
   - Select payload defn. left side, right side
   - zip, weatherCit, Country
1. Add invoke policy
   - http://weather.api.yahoo.com
   - Set method to POST
   - Add set-variable
     - Header
     - SOAP OpID (TBD)
   - Add response map (zip -> zip, weatherCity -> city, XML -> json)

### Invoking a Micro Service from an API Proxy

TBD

### Deploying an assembly to Bluemix
