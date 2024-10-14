---
title: Data Import (Tailored Datasets)
slug: CZeV-d
createdAt: Thu Jul 18 2024 12:23:56 GMT+0000 (Coordinated Universal Time)
updatedAt: Thu Sep 19 2024 13:37:04 GMT+0000 (Coordinated Universal Time)
---

## Goal

Ingest Retail industry large events data in Experience Platform datasets.

## Pre-requisites

1. Schemas setup using [dsn.adobe.com/quick-setup](https://dsn.adobe.com/quick-setup)
2. Data from [Tools > Tailored Datasets](https://dsn.adobe.com/tools/datasets) is compatible in "***Adobe Demo System Shared***" Org. ( `demosystem4` )&#x20;
   (*In order to ingest data in other org refer ****Updating data for other org**** section.*)

## Data-files

:::hint{type="warning"}
1. Enabling datasets for "Profile" adds cost for identity services. Unless you need to show the profiles dashboard/events/audience/profile-scores; it's advisable to keep datasets disabled for "Profile".
2. You may choose to leverage existing datasets (*which is enabled for "Profile" by default*) OR choose to create new datasets. Refer the "BASE SCHEMA" columns in below table.
3. You may choose to use the output generated for **AJO**.
4. You **must create new datasets** to ingest "**AJO**" related data files.
5. To ingest "profiles**.csv**", use "Workflow" UI (**Map CSV to XDM**) feature. Choose the attributes to include.&#x20;
   Profile attributes, other than identities; such as, `email`, `crmId`, `loyaltyId` etc. are open to be customized for your use case. You may use excel / numbers expression to randomly populate data for existing column or new columns.
:::

| **FILE NAME**                | **BASE SCHEMA**                                                |
| ---------------------------- | -------------------------------------------------------------- |
| `WEBSITE-EE-*.json`          | Demo System - Event Schema for Website (Global v1.1)           |
| `MOBILE-EE-*.json`           | Demo System - Event Schema for Mobile App (Global v1.1)        |
| `CALL-CENTER-EE-*.json`      | Demo System - Event Schema for Call Center (Global v1.1)       |
| `CHATBOT-EE-*.json`          | Demo System - Event Schema for Stackchat Chatbot (Global v1.1) |
| `OFFLINE-EE-*.json`          | Demo System - Event Schema for POS (Global v1.1)               |
| `AJO-TRACKING-EVENTS-*.json` | AJO Email Tracking Experience Event Schema                     |
| `AJO-FEEDBACK-EVENTS-*.json` | AJO Message Feedback Event Schema                              |
| `AJO-STEP-EVENTS-*.json`     | Journey Step Event schema for Journey Orchestration            |
| `AJO-ENTITY-RECORDS-*.json`  | AJO Entity Record Schema                                       |
| `profiles.csv`               | Demo System - Profile Schema for CRM (Global v1.1)             |

:::hint{type="info"}
***IDENTITY MAPPING***

To unify the events from multiple datasets, you need to choose identiy key, which allows to stitch data.

- For "**AJO**" related datasets choose `IdentityMap` & Select `CRM ID` as the identity key.
- For other datasets like web, mobile, chatbot, call-center & offline; choose: `<_tenantId>.identification.core.crmId`
:::

## Entity relationship

![Demo System Next - Entity Relationship](../../assets/NXbLtbNUHqcezf3QGwYNX-ej1Pzga-XldtqB44TWAIG-20240816-142004.jpg "Demo System Next - Entity Relationship")

## Data ingestion

Referring above mentioned schemas, you may choose to use existing datasets or you may create new dataset. Enabling datasets for Profile, is optional for data ingestion. If you’re planning to search for the uploaded Profiles or show customer experience events in Profile details tab; then, dataset should be enabled for Profile.

Open the dataset and drag-drop the JSON files to start ingestion process. While uploading files, check the file names, it should match as mentioned above. You can *upload multiple files* for a dataset.&#x20;

### Event types

The pre-generated experience events has the following `eventType` values associated to output result. You could leverage this list to define dimensions (*in case of CJA*) or custom events (*in case of Intelligent Service instance*) to improve result

| **Event title**        | **Event type**                 |
| ---------------------- | ------------------------------ |
| Ad clicks              | `advertising.clicks`           |
| Web searches           | `commerce.searches`            |
| Web logins             | `web.application.logins`       |
| Web registrations      | `web.application.registration` |
| Signup Step #1         | `loyalty.signups.step1`        |
| Signup Step #2         | `loyalty.signups.step2`        |
| Signup Step #3         | `loyalty.signups.step3`        |
| Page views             | `web.webpagedetails.pageViews` |
| Product views          | `commerce.productViews`        |
| Product interests      | `commerce.saveForLaters`       |
| Add to cart            | `commerce.productListAdds`     |
| Cart views             | `commerce.productListViews`    |
| Checkouts step #1      | `commerce.checkouts.step1`     |
| Checkouts step #2      | `commerce.checkouts.step2`     |
| Checkouts step #3      | `commerce.checkouts.step3`     |
| Product purchases      | `commerce.purchases`           |
| Product orders         | `commerce.orders`              |
| Product returns        | `commerce.returns`             |
| Mobile App Launch      | `mobileApp.launches`           |
| Mobile App Logins      | `mobileApp.logins`             |
| Outlet visits          | `pos.visits`                   |
| Dial in                | `callcenter.dialIns`           |
| Grievance calls        | `callcenter.dialIns.grievance` |
| Service requests       | `callcenter.dialIns.services`  |
| Product enquiries      | `callcenter.dialIns.enquiries` |
| Order enquiries        | `callcenter.order.enquiries`   |
| Bot interactions       | `bot.interaction`              |
| Offer presented        | `offer.presented`              |
| Offer accepted         | `offer.accepted`               |
| Offer rejected         | `offer.rejected`               |
| Message sent           | `message.feedback`             |
| Message opens / clicks | `message.tracking`             |





## Updating data for other org

These pre-generated event data have **Adobe Demo System Shared** Org **tenant-id**, `_demosystem4`, referred in XDM.&#x20;

So, to ingest these output files in other Org, you would need to replace the existing **tenant-id** with the target Org.

:::hint{type="warning"}
*** Mac OS***:

- Open "Terminal" app
- Navigate to the data extracted directory path:
  `cd folder-path-where-output-file-availabe`
  Example: `cd Documents/2024-25/XEGen-IS-R/luma-events-latest/EVENTS`
- This directory / folder should containt only the `.json`** **files.
- Execute the following command to replace:
  `find . -type f -name "*.json" -exec sed -i '' 's/\"_demosystem4\"/\"_NEW_TENANT\"/g' {} +`
  Example: `find . -type f -name "*.json" -exec sed -i '' 's/\"_demosystem4\"/\"_demoamericas26\"/g' {} +`
:::

:::hint{type="warning"}
 ***Windows:***

- Open command prompt or power-shell
- Navigate to the data extracted directory path:
  `cd folder-path-where-output-file-availabe`
  Example: `cd Documents\2024-25\XEGen-IS-R\luma-events-latest\EVENTS`
- This directory / folder should containt only the `.json`** **files.
- Execute the following command to replace:
  `for /r %f in (*.json) do powershell -Command "(Get-Content -Path '%f') -replace '\"_demosystem4\"', '\"_demoamericas26\"' | Set-Content -Path '%f'"`
:::



