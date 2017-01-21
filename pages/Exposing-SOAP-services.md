---
title: Exposing SOAP services as REST APIs
keywords:
tags:
sidebar: 
permalink: /Exposing-SOAP-services.html
summary:  Today, “web services” usually means REST (Representational state transfer) APIs using JSON as the data exchange format.  However, the first generation of web services was built using SOAP (Simple Object Access Protocol), a standard protocol based on XML.  In many enterprises, SOAP web services are still important assets, and some APIs are only available via SOAP.
---

{% assign content = site.data.soap %}


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
