---
title: Versioning your API Connect Project
layout: tutorial
keywords:
sidebar:
permalink: /Versioning.html
summary:
---

Follow these steps:

Select the Products tab in API Designer. The Products tab opens.

Click **Add** and then click **New product**.

In the **product** window, complete the following steps:

1. In the **Product template** field, select Default if you want to use the template defined as the default, to create the Product definition. This can either be the default `.hbs` template file provided with the developer toolkit, or another template file that you have configured as the default by using configuration variables. You can also select a custom template that you created. For information about template files and configuration variables, see Creating and using API and Product definitions templates and Toolkit command summary.
1. Specify a title, name, and version for the Product.
Note: The Name field can contain only lowercase alphanumeric characters (a-z and 0-9), and hyphen characters (-). You can't use a hyphen as the first or last character in the name.
1. Click **Create product**. The Design tab for the new Product opens.

Optional: Enter description, contact, license, and terms of service information for the Product in the Info section.

In the **Visibility** section, specify the users that you want the Product to be visible to. You can choose Public, Authenticated users, or Custom.

If you select Custom, type the name of the organization or community that you want the Plans in the Product to be visible to in the Type to add field. For information about how to create and manage organizations or communities, see Administering Developer organizations.

Specify the users that can subscribe to the Product. You can choose Authenticated users or Custom.

If you select Custom, type the name of the organization or community that you want to be able to subscribe to the Plans in the Product in the Type to add field. For information about how to create and manage organizations or communities, see Administering Developer organizations

In the **APIs** section, specify the APIs that you want to include in the Product.

- Click the Add API icon The Add API icon.
- Select the APIs that you want to include, then click Apply. The selected APIs are listed.

{% include note.html content = "To make an API available to application developers, you must include it in a Plan.
" %}

Add one or more Plans to the Product:

- Click the Add Plan icon The Add Plan icon.
- Expand the new Plan that has been created. If you have already added APIs to your Product, these are automatically included.
- Rename your Plan in the Title and Name fields, and optionally add a description.

{% include note.html content = "A Default Plan is automatically created for you if you do not want to create your own, and any APIs that you selected in the previous step are automatically included in this Plan. You can clear the check box for any API to exclude it from the Plan, but at least one API must be included because a Product cannot be staged if it includes any Plans that do not include APIs. If you decide not to use the Default Plan, you must delete it.
" %}

Verify that the APIs you require are included in the Plan:

- Expand the Plan to which you want to add APIs.
- Under APIs included, ensure that the check boxes of the APIs you require are selected. If there are APIs already selected, and you do not want them included in the Plan you are editing, clear their check boxes.

{% include note.html content = "If you add the same API to more than one Plan, and the same Application (client ID) signs up for multiple Plans that contain the same API, the Gateway server cannot determine which Plan rate limit should be applied. If you anticipate that an API will be shared by an Application, a proxy API should be defined so that the correct Plan rate limit can be applied.
" %}

Optional: Select which operations from an API to include in the Plan.

- Hover the cursor over the API that contains the operation, and click the Show operations icon Show operations icon.
- Select or clear the check boxes for the operations you want to include or exclude.
Optional: Add a rate limit to your Plan.
Click the Add new rate limit icon The Add new rate limit icon, and then specify the rate limit that you want to apply. You can set multiple rate limits, at second, minute, hour, day, and week time intervals.

**DataPower Gateway only**
To add burst limits to your Plan, so that you can prevent usage spikes that might damage infrastructure, click the Add new burst limit icon The add new burst limit icon, and then specify the burst limit that you want to apply. You can set multiple burst limits, at second and minute intervals. To remove a rate or burst limit, click the Delete rate limit or Delete burst limit icon The delete rate or burst limit icon.

If the Enforce hard limit check box is selected, the Plan will stop applications from calling the API after reaching the rate limit. Otherwise, you'll see a warning such this in the log file:

```
logger.warn('Rate limit (%d/s) exceeded but not rejected', limit);
```

{% include note.html content = "Applying a rate limit at the Plan level creates a default rate limit that is shared across all the operations within the Plan. If you need to set specific rate limits for specific operations, you must set these within the operations themselves and these settings will override the setting at the Plan level.
The test application that is used by the API Manager test tool is not subject to rate limits if you have enabled automatic subscriptions for the Catalog in which you are testing. For more information, see Working with Catalogs
For information about setting specific rate limits for operations, see step 14.
" %}

**Optional**: Specify whether your Plan requires subscription approval. If you want subscriptions by developers to require approval through the API Manager user interface, select Require subscription approval; otherwise, ensure the check box is cleared.

**Optional**: Add a rate limit to an operation.

- Hover the cursor over the API that contains the operation, and click the Show operations icon Show operations icon.
- Hover the cursor over the operation that you want to apply a rate limit to, and click Override rate limit.
- Specify the rate limit that you want to apply. If the Enforce hard limit check box is selected, the Plan will stop applications from calling the operation after reaching the rate limit; otherwise, a warning will be presented.
- Optional: To set additional rate limits, click the Add new rate limit icon The Add new rate limit icon for the operation, and then specify the rate limit that you want to apply. You can set multiple rate limits, at second, minute, hour, day, and week time intervals.

Click **Save** to save your changes.

## References

Leverage:

- [Working with Products in the API Designer](http://www.ibm.com/support/knowledgecenter/SSFS6T/com.ibm.apic.toolkit.doc/capim_products.html)
- [Creating a new version of your Product](http://www.ibm.com/support/knowledgecenter/SSFS6T/com.ibm.apic.toolkit.doc/product_versions.html)
- []()
