---
title: Create a new data source
keywords:
layout: tutorial
sidebar: microservice
permalink: /microservice-2.html
next: true
summary: A data source connects your microservice to a back-end data store such as a database, a SOAP service, or REST API. A project may have any number of data sources.
---

Follow these steps to create a new data source:

1. Click **Data sources** to display all your data sources.  Of course, if you haven't created any data sources yet, you won't see any!  
1. Click **Add** to add a new data source.
1. Type a name for your data source.  Enter "gs-datasource" or use something else if you prefer. Then click **New**.

{% include image.html file="microservices2.gif" alt="Creating a new LoopBack data source" %}

After you create the data source, you'll see the Data Source properties page.
For now, leave all the defaults here.  The "in-memory db" connector stores data in memory for development and testing.  Later, you can change this to MongoDB, MySQL, or [any LoopBack data source connector](http://loopback.io/doc/en/lb2/Connectors-reference.html).

{% include image.html file="microservices3.gif" alt="Creating a new LoopBack data source" %}

Click **All Data Sources** to return to the Data Sources view.
