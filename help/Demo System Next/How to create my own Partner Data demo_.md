---
title: How to create my own Partner Data demo?
slug: s9oQ-how-to-create-my-own-partner-data-demo
createdAt: Thu Oct 05 2023 12:26:14 GMT+0000 (Coordinated Universal Time)
updatedAt: Fri Oct 20 2023 13:13:35 GMT+0000 (Coordinated Universal Time)
---

There are several scenarios prepared for you on DSN public-securfinancial sandbox. You can learn about them here:&#x20;

[Partner Data: On-Site Personalization for Unknown Visitors](<../Demo System Next/Partner Data_ On-Site Personalization for Unknown Visitors.md>)

[Partner Audience Expansion](<../Demo System Next/Partner Audience Expansion.md>)

[Partner Enrichment of Known Customers](<../Demo System Next/Partner Enrichment of Known Customers.md>)

[Partner Data: On-Site Personalization for Unknown Visitors](<../Demo System Next/Partner Data_ On-Site Personalization for Unknown Visitors.md>)

If you want to build your own version, using sandbox you have access too there are several assets that you can use.

1. In quick setup <https://dsn.adobe.com/quick-setup> every preset has additional option to install Partner related schemas. You can also just installed this schemas yourself by going to advanced section and selecting "Partner" in the Core AEP secion.

![](../../assets/t7laxGZvwyAnEUe7ysFsG_image.png)

The action above will create:

- 2 field groups\:Partner Enrichment and Partner Prospecting
- 2 schemas: Demo System - Partner Data Enrichment Schema (Global v2.0), Demo System - Partner Data Prospecting Schema (Global v2.0),
- 2 datasets: Demo System - Partner Data Enrichment Dataset (Global v2.0), Demo System - Partner Data Prospecting Dataset
- 1 identity: Demo System - PartnerId, "code": "partnerId"
- Schema descriptros for partnerId
- Few segments: High Earning Homeowners, Loyalty Program Prospects, New Channel Prospects
- 1 additional prospect audience is on the way: New Demographic Prospects

2\. You can also use **data generators** to create data for the Demo System - Partner Data Enrichment Dataset (Global v2.0)

- Go to <https://dsn.adobe.com/data>
- Select the dataset name: Demo System - Partner Data Enrichment Dataset
- Select your org

![](../../assets/0njqgiZ4XgqAt2QAO_WMM_image.png)



This is a sample file that was created:

[](../../assets/1uRyQentGqJ09oRZcjpeR_partnergenericglobalprofiles.json)

Drag and drop the generated file to your dataset. This profiles can be used to enriched the already existing profiles with partner Id - more details in [Partner Enrichment of Known Customers](<../Demo System Next/Partner Enrichment of Known Customers.md>) scenario.

3\. Attach the Launch property to your website. It has two rules: Get Partner Data and Send Partner Date (learn more about in the on-site personalization scenario flow for SecurFinancial)

4\. Activate the required segmnets for your campaign

4\. Build the Activity in Target using the segments
