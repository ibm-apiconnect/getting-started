---
title: Publish to the API Manager
layout: tutorial
sidebar: publishing
permalink: /publishing-3.html
summary:
---

In the API Designer, complete the following steps:

1. Click **APIs**.
1. Select **my-notes**.
1. Click **Assemble**.
1. In the Assembly editor, click the Filter policies icon:
{% include image.html file="filter-policies-icon.png" alt="Filter policies" %}
1. Select **DataPower Gateway policies**.
1. Click **Save** to save the API.
1. Next, you need to publish to the API Manager. Click **Publish** and select the following options: **Stage or Publish products**, **Select specific products**, and **my-notes**.
1. Return to the Bluemix Dashboard. You will see the application tile in the Applications section:
{% include image.html file="my-notes-bm.png" alt="Bluemix application tile" %}

Now you can use API Manager to publish the API product to your Developer Portal, so that application developers can access it. Follow the instructions in Publishing an API with API Manager. You can also use the API manager to manage your APIs by configuring authentication measures, setting rate limits, and enforcing policies.
