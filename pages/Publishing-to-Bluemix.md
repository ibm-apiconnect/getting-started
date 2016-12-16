---
title: Publishing your API to Bluemix
keywords:
toc: false
sidebar: gs_sidebar
permalink: /Publishing-to-Bluemix.html
summary: You can stage and publish a project to Bluemix using the API Designer.
---
{% assign content = site.data.bluemix.intro %}

<div markdown="1" class="alert alert-info" role="alert"><i class="fa fa-info-circle"></i>
<b>Note:</b> {{ content.caveat }}
</div>

{{ content.summary }}

{% assign content = site.data.bluemix.configure %}
{% include section-head.md %}

1. {{content.login}}  
1. {{content.apis}}
1. {{content.manager}}
1. {{content.create_service}}
1. {{content.dashboard}}

{% assign content = site.data.bluemix.publish %}
{% include section-head.md %}

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
