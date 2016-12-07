---
title: Creating your first microservice
toc: false
keywords:
tags:
sidebar: gs_sidebar
permalink: Creating-your-first-microservice.html
summary: You can quickly create a microservice in the API Designer using the LoopBack Node.js framework.
---

To create a microservice using LoopBack, follow these steps:

{% assign content = site.data.microservice %}

<ol>
{% for item in content %}
  {% capture id %}{{item[0]}}{% endcapture %}
  {% assign content_item = content[{{id}}] %}
  <li>
    <b><a href="#{{content_item.title | replace: " ", "-" | downcase}} ">{{content_item.title }}</a></b>
    <br/>{% capture summary_md %} {{content_item.summary }} {% endcapture %} {{ summary_md | markdownify }}
  </li>
{% endfor %}
</ol>

{% assign content = site.data.microservice.create_project %}

## {{ content.title }}

{{ content.summary }}

<div markdown="1" class="alert alert-info" role="alert"><i class="fa fa-info-circle"></i>
<b>Note:</b> {{ content.caveat }}
</div>

{{ content.project_pane_open }}

![](http://content.screencast.com/users/RandMck/folders/Jing/media/47661bf6-dcd4-4012-89e3-88e1798a029c/00000535.png)

{{ content.create_project }}

![](http://content.screencast.com/users/RandMck/folders/Jing/media/49cd1820-9446-4242-b978-8cd3d0f7a1f7/00000537.png)

{{ content.project_type }}

![](http://content.screencast.com/users/RandMck/folders/Jing/media/4ac5f21a-da69-4cb0-b3c9-6c3aef98717f/00000518.png)

{{ content.project_dialog }}

![](http://content.screencast.com/users/RandMck/folders/Jing/media/a65a6a38-cfc6-439f-b5cd-ef4828dff90a/00000519.png)

{% assign content = site.data.microservice.create_datasource %}

## {{ content.title }}

{{ content.summary }}

{{ content.display_datasources}}

![](http://content.screencast.com/users/RandMck/folders/Jing/media/e9231d8e-9c73-41e4-9a5c-85810f1d2899/00000538.png)

{{ content.add_ds}}

![](http://content.screencast.com/users/RandMck/folders/Jing/media/cde360b9-85f9-4e12-8900-2c5a776d88fe/00000520.png)

{{ content.name_ds}}

![](http://content.screencast.com/users/RandMck/folders/Jing/media/4c23c299-0278-4846-a71e-01f8efb017ee/00000521.png)

{{ content.ds_dialog}}

{{ content.return_ds_view}}

![](http://content.screencast.com/users/RandMck/folders/Jing/media/a03a7cc4-4484-40cc-bfe3-c16376d98fa3/00000539.png)

{% assign content = site.data.microservice.create_model %}

## {{ content.title }}

{{ content.summary }}

{{ content.display_models}}

![](http://content.screencast.com/users/RandMck/folders/Jing/media/98208e17-d3e5-4edb-9ccd-eda6006c05b5/00000540.png)

{{ content.add_models }}

![](http://content.screencast.com/users/RandMck/folders/Jing/media/ba88ffb4-7ef2-4eee-ae44-1b3158cab5fd/00000523.png)

{{ content.name_model }}

![](http://content.screencast.com/users/RandMck/folders/Jing/media/63b08253-caa2-402a-a809-33d8edf99762/00000541.png)

{{ content.model_dialog }}

![](http://content.screencast.com/users/RandMck/folders/Jing/media/d37b1aef-e6f0-4b8c-a2b2-ca6ec20679a4/00000542.png)

{% assign content = site.data.microservice.add_props %}

## {{ content.title }}

{{ content.summary }}

{{ content.add_prop }}

![](http://content.screencast.com/users/RandMck/folders/Jing/media/c0c562ac-e653-4d81-8ff3-4a457f9f9719/00000524.png)

{{ content.property_settings }}

{{  content.add_prop2}}

![](http://content.screencast.com/users/RandMck/folders/Jing/media/c0c562ac-e653-4d81-8ff3-4a457f9f9719/00000524.png)

{{  content.prop_settings2 }}

![](http://content.screencast.com/users/RandMck/folders/Jing/media/ceebcc3e-7abd-4069-bb9d-e0a403e1a45e/00000525.png)

{{ content.save_model }}

![](http://content.screencast.com/users/RandMck/folders/Jing/media/6e76b578-cb57-416c-a326-02995548d6d5/00000526.png)

{{ content.return_models_view}}

![](http://content.screencast.com/users/RandMck/folders/Jing/media/ecf0cf9a-ea78-4c69-bbb4-d090eda558b6/00000543.png)

{% assign content = site.data.microservice.run_project %}

## {{ content.title }}

{{ content.summary }}

: Scroll down and click to call the operation.
view_results: After clicking **Call Operation**, scroll down to see the results.

{{ content.run_project }}

![](http://content.screencast.com/users/RandMck/folders/Jing/media/cec33edf-0a9f-4a06-b727-b6975dfcca0e/00000544.png)

<div markdown="1" class="alert alert-info" role="alert"><i class="fa fa-info-circle"></i>
<b>Note:</b> {{ content.note }}
</div>

{{content.logs}}

![](http://content.screencast.com/users/RandMck/folders/Jing/media/23ebb54b-fdd1-4787-b3fd-5d1247478e42/00000545.png)

{{ content.explore }}

![](http://content.screencast.com/users/RandMck/folders/Jing/media/0deb803e-9235-4833-bf71-594b768ce307/00000546.png)

{{ content.post }}

![](http://content.screencast.com/users/RandMck/folders/Jing/media/124794d6-4037-490a-a24c-2ca43ffb668e/00000549.png)

{{ content.generate }}

{{ content.call_op }}

![](http://content.screencast.com/users/RandMck/folders/Jing/media/d1fe5977-d80a-4a2b-9919-801bffdacf87/00000553.png)

{{ content.get }}

![](http://content.screencast.com/users/RandMck/folders/Jing/media/3cc0f0dd-2177-4b77-ae92-7198b1f805c1/00000551.png)

{{ content.call_op2 }}

![](http://content.screencast.com/users/RandMck/folders/Jing/media/17c04db8-a06f-4bb7-9899-a1517fd6855a/00000552.png)

{{ content.view_results }}
After clicking **Call Operation**, scroll down to see the results.

![](http://content.screencast.com/users/RandMck/folders/Jing/media/a798e019-dba6-401b-812d-4f28d377dee6/00000534.png)

> DO WE STILL WANT TO DO THIS?
> ... Show the generated Swagger.
