---
title: Creating your first Product
layout: tutorial
keywords:
permalink: /First-product.html
summary: Create a Product to collect a set of APIs and Plans into one offering that you make available to your developers.
---

## Creating a Product in the API Designer

Create a Product to collect a set of APIs and Plans into one offering that you make available to your developers. A Plan includes rate limit settings that can be applied to the Plan as a whole, or specified for each operation in an API. Through Products and Plans, you have greater control over what APIs your developers have access to.

## Before you begin

Define your APIs. For more information, see [Creating API definitions](http://www.ibm.com/support/knowledgecenter/SSFS6T/com.ibm.apic.toolkit.doctask_apionprem_composing_apis.html).

Anybody using the API Designer can perform all actions within it. However, when staging or publishing a Product, permissions will be enforced by API Connect. For more information about user roles and permissions, see [Administering user access](http://www.ibm.com/support/knowledgecenter/SSFS6T/com.ibm.apic.apionprem.doc/user_access_admin.html).

{% include tip.html content="  As well as using the method described in this task, you can also create a Product when you create an API. If you create an API by using the developer toolkit command line editor, a Product is automatically created for you. You can then change any of the Product settings by opening your new Product in the **Products** page of the API Designer.
" %}

## Procedure

To create a Product, complete the following steps:

1.  Run API Designer.
2.  Select the **Products** tab in API Designer. The **Products** tab opens.
3.  Click **Add** and then click **New product from scratch**.  

4.  From the **New product from scratch** window, complete the following steps:
    1.  In the **Product template** field, select **Default** if you want to use the template defined as the default, to create the Product definition. This can either be the default `.hbs` template file provided with the developer toolkit, or another template file that you have configured as the default by using configuration variables. You can also select a custom template that you created. For information about template files and configuration variables, see [Creating and using API and Product definitions templates](http://www.ibm.com/support/knowledgecenter/SSFS6T/com.ibm.apic.toolkit.doc/task_apim_cli_templates.html). You can use template files when creating API and Product definitions. Template files are Handlebars templates containing variables of the form &#123;&#123;`variable-name`&#125;&#125; that are substituted with values when you create the API or Product definition. and [Toolkit command summary](http://www.ibm.com/support/knowledgecenter/SSFS6T/com.ibm.apic.toolkit.doc/rapim_cli_command_summary.html).
    2.  Specify a title, name, and version for the Product.

        {% include note.html content="The **Name** field can contain only lowercase alphanumeric characters (a-z and 0-9), and hyphen characters (-). A hyphen cannot be used as the first or last character in the name.
        " %}

    3.  Click **Create product**. The **Design** tab for the new Product opens.
5.  Optional: Enter description, contact, license, and terms of service information for the Product in the **Info** section.
6.  In the **Visibility** section, specify the users that you want the Product to be visible to. You can choose **Public**, **Authenticated users**, or **Custom**.  <br/>If you select **Custom**, type the name of the organization or community that you want the Plans in the Product to be visible to in the **Type to add** field. For information about how to create and manage organizations or communities, see [Administering Developer organizations](http://www.ibm.com/support/knowledgecenter/SSFS6T/com.ibm.apic.toolkit.doc/apionprem_manage_consumerorgs.html).

7.  Specify the users that can subscribe to the Product. You can choose **Authenticated users** or **Custom**. <br/>  If you select **Custom**, type the name of the organization or community that you want to be able to subscribe to the Plans in the Product in the **Type to add** field. For information about how to create and manage organizations or communities, see [Administering Developer organizations](http://www.ibm.com/support/knowledgecenter/SSFS6T/com.ibm.apic.apionprem.doc/apionprem_manage_consumerorgs.html)

8.  In the **APIs** section, specify the APIs that you want to include in the Product.
    1.  Click {% include inline_image.html file="plus_icon.jpg" alt="Add icon" %} **Add API** .
    2.  Select the APIs that you want to include, then click **Apply**. The selected APIs are listed.

    {% include tip.html content=" To make an API available to application developers, you must include it in a Plan.
    " %}

9.  Add one or more Plans to the Product.
    1.  Click  {% include inline_image.html file="plus_icon.jpg" alt="Add icon" %} **Add Plan**.
    2.  Expand the new Plan that has been created. If you have already added APIs to your Product, these are automatically included.
    3.  Rename your Plan in the **Title** and **Name** fields, and optionally add a description.

    {% include note.html content="A Default Plan is automatically created for you if you do not want to create your own, and any APIs that you selected in the previous step are automatically included in this Plan. You can clear the check box for any API to exclude it from the Plan, but at least one API must be included because a Product cannot be staged if it includes any Plans that do not include APIs. If you decide not to use the Default Plan, you must delete it.
    " %}

10.  Verify that the APIs you require are included in the Plan:
  - Expand the Plan to which you want to add APIs.
  - Under **APIs included**, ensure that the check boxes of the APIs you require are selected. If there are APIs already selected, and you do not want them included in the Plan you are editing, clear their check boxes.  If you add the same API to more than one Plan, and the same Application (client ID) signs up for multiple Plans that contain the same API, the Gateway server cannot determine which Plan rate limit should be applied. If you anticipate that an API will be shared by an Application, a proxy API should be defined so that the correct Plan rate limit can be applied.


11.  **Optional**: Select which operations from an API to include in the Plan:
  -  Hover the cursor over the API that contains the operation, and click {% include inline_image.html file="downarrow.jpg" alt="Delete icon" %} **Show operations**.
  -  Select or clear the check boxes for the operations you want to include or exclude.

12.  **Optional**: Add a rate limit to your Plan:
  - Click {% include inline_image.html file="plus_icon.jpg" alt="Add icon" %} **Add new rate limit** , and then specify the rate limit that you want to apply. You can set multiple rate limits, at second, minute, hour, day, and week time intervals.
  - **DataPower Gateway only** To add burst limits to your Plan, so that you can prevent usage spikes that might damage infrastructure, click {% include inline_image.html file="plus_icon.jpg" alt="Add icon" %} **Add new burst limit**, and then specify the burst limit that you want to apply. You can set multiple burst limits, at second and minute intervals. To remove a rate or burst limit, click {% include inline_image.html file="delete_icon_dark.png" alt="Delete icon" %} **Delete rate limit** or **Delete burst limit** .
  - If the **Enforce hard limit** check box is selected, the Plan will stop applications from calling the API after reaching the rate limit. Otherwise, a warning such as the following message will be presented in the log file: ```logger.warn('Rate limit (%d/s) exceeded but not rejected', limit);```

13.  **Optional**: Specify whether your Plan requires subscription approval. If you want subscriptions by developers to require approval through the API Manager user interface, select **Require subscription approval**; otherwise, ensure the check box is cleared.

14.  Click **Save** to save your changes.

{% include note.html content="Applying a rate limit at the Plan level creates a default rate limit that is shared across all the operations within the Plan. If you need to set specific rate limits for specific operations, you must set these within the operations themselves and these settings will override the setting at the Plan level.

The test application the API Manager test tool uses is not subject to rate limits if you have enabled automatic subscriptions for the Catalog in which you are testing. For more information, see [Working with Catalogs](http://www.ibm.com/support/knowledgecenter/SSFS6T/com.ibm.apic.apionprem.doc/conref_working_with_env.html).
" %}

## What to do next

Stage your Product to a Catalog. For more information, see [Staging a Product](http://www.ibm.com/support/knowledgecenter/SSFS6T/com.ibm.apic.toolkit.doc/task_deploy_product_offline.html). Stage a Product to a Catalog to create a specific version of that Product, before publishing. When a Product is in the staged state, it is not yet visible to, or subscribable by, any developers.

## See also

[Creating a Product definition file](http://www.ibm.com/support/knowledgecenter/SSFS6T/com.ibm.apic.toolkit.doc/task_apim_cli_product_yaml.html) (CLI). Also, children of this article.
