---
title: Publish to Bluemix
layout: tutorial
sidebar: publishing
permalink: /publishing-2.html
summary: Once you've configured Bluemix, then you can publish your API to Bluemix from API Designer.
---

Follow these steps:

1. In the API Designer, click **Publish** then **Add and Manage Targets**.
1. Click **Add IBM Bluemix target**.
1. Select a region, organization and catalog (use “Sandbox” for now). Click **Next**.
1. Type the application name (“my-notes”) then click **+**.
1. Select the application you just added and click **Save**.
1. Click **Publish** again and select the target you just added.
1. You will see the Publish Options dialog (You may see different options, depending on your configuration and what you have created): {% include image.html file="bm-publish.png" alt="Bluemix publish options" %}
1. Select the following:
  - **Publish application** to publish the current application to the selected target.
  - **Stage or Publish products** to stage all of the products.
  - **Select specific products** to choose specific products.
  - **my-notes** to select the product you just created.
1. Click **Publish** then select the target you previously added. The console where you started the API Designer will display a number of messages. If the application is successfully published, then the final messages will be similar to this:

```
Runtime published successfully.
Using buildpack: SDK for Node.js(TM) (ibm-node.js-4.4.3, buildpack-v3.3-20160428-1409)
Management URL: https://new-console.ng.bluemix.net/apps/ca3283b0-525c-488d-993b-3ab72fca78d0
API target urls: apiconnect-ca2343b0-525c-477d-993b-3ab72fca78d0.youremail-dev.apic.mybluemix.net
API invoke tls-profile: client:Loopback-client
```
