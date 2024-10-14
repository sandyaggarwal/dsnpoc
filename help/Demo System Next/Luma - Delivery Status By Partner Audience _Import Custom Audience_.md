---
title: Luma - Delivery Status By Partner Audience (Import Custom Audience)
slug: CeuU-luma
createdAt: Tue Jun 11 2024 09:40:59 GMT+0000 (Coordinated Universal Time)
updatedAt: Tue Sep 17 2024 10:00:54 GMT+0000 (Coordinated Universal Time)
---

# Introduction

In the Adobe Experience platform to create an Audience we have some prerequisites:

1. To bring base data in Adobe Experience Platform we need to have schemas and datasets against them to hold that data.
2. Segmentation logic or definition to build an audience.

![](../../assets/TT7G7NFCEhc1dmwR1hf6o_screenshot-2024-06-11-at-25945-pm.png)

## Import/Upload of Custom Audience

Adobe Experience Platforms provides the capability to import custom audiences from outside sources. If you have a system that holds your data and provides segmentation capability. Then, you can import that data into the Adobe Experience platform using the import audience capability and utilize it further for marketing.



![](../../assets/XYBzsmhYrViytr2kLXQvR_screenshot-2024-06-11-at-30007-pm.png)

## Access

To demonstrate the upload of custom audience capability you need to have access to the **import audience** tab under **Customer > Audience** tab. If not then you need to have access for the same.

## Demo Storyline

As Luma is a retail brand and it has outsourced its delivery services to 3rd party vendor. But Luma wants to keep track of the delivery status of the order inside the Adobe Experience Platform and whenever required can inform them about any delays or changes or even in case when a customer inquires about his/her order.

As 3rd party vendor uses a different system for keeping data of the delivery status of the order. So, Luma decides to bring this data into the Adobe Experience Platform by uploading this data to an audience by using the Import Custom Audience feature and sending out the communication using AJO for delivery status and upsell of products.

## STEPS:

1. Go to **Adobe Experience Platform** then under **Customer > Audiences**.
2. Click on **Import Audience**.
3. Drop or upload your CSV file and then click on **next**.
4. Fill in the **Audience name, description, Primary Identity, and Identity namespace**.
5. Click on **next** to preview what you have configured in previous steps configured.
6. Click **Finish** to complete the process and your new segment will be created.

You can see your segment created in the list and the origin tab will show **Custom upload**.

![](../../assets/nhd7ZRQmXHjyBez9NK2Ik_screenshot-2024-06-18-at-53606-pm.png)

## Important Notes:

1. There is a file limit of 1GB.
2. The 10-column limit for the file.
3. Uploading audiences can augment existing profiles and create new ones.
4. These are available for AJO campaigns or Journeys.

## Template Download:

[](../../assets/XLVhZF9rcf_wJRiL5Lnsq_import-audience-template.csv)

