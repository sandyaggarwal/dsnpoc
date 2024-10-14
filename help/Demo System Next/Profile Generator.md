---
title: Profile Generator
slug: ABwX-profile-data-generators
createdAt: Fri Oct 27 2023 13:13:16 GMT+0000 (Coordinated Universal Time)
updatedAt: Tue Nov 28 2023 11:09:50 GMT+0000 (Coordinated Universal Time)
---

Demo System Next features a Profile Generator. It delivers a file with requested number of profiles that can later be imported into AEP datasets. You can access this tool at <https://dsn.adobe.com/tools/profile-generator>

:::hint{type="info"}
Behind the scenes, profile generator is using Mockaroo with predefined fields matching the Global Schemas. Let us know if you are interested in extending the current data models and values.
:::

Each available industry-specific schema matches a dataset based on Global Schema - you might need to use the Quick Setup tool to configure your sandbox with appropriate Field Groups.

## Supported profiles:&#x20;

Retail, FSI, Healthcare (international and USA), Media, Telco and Travel

![](../../assets/q335BmmuPOlRbgysmluki_image.png)



## Generate Profiles UI

![](../../assets/3xl8yzRT1xXhjrElnhxrr_image.png)

First section allows you to specify the format of unique email addresses that will be generated for each profile. To clarify naming, email address is built with the following parts: \<recipient>+\<alias>@\<domain>.&#x20;

**Base email **will be modified by adding an alias with the ordinal number of the generated profile. If you specified an alias in **base email**, ordinal number will be appended to it. A preview of first 3 email addresses is displayed below this field.

In the second section, you can select a **Dataset name **that the JSON file will be uploaded to, **Data variant** - generally an industry,  provide required **tenant ID **and choose how many profiles you need. The more profiles, the larger the downloaded file and longer wait time. Current upper limit is 5000 records.

Note: all generated profiles require "**Test Profiles**" Field Group (mixin) to be installed in your instance. If you are using quick setup there should be no problem with that.

Downloaded JSON file can be dragged & dropped into the right DataSet in AEP. Generated profiles will be available to use once AEP finishes processing them.

Downloaded CSV can be mapped to a dataset using the standard import workflow in AEP.
