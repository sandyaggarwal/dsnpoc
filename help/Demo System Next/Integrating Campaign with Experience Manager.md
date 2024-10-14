---
title: Integrating Campaign with Experience Manager
slug: rqWK-aem
createdAt: Thu Aug 22 2024 12:24:14 GMT+0000 (Coordinated Universal Time)
updatedAt: Fri Aug 30 2024 13:48:06 GMT+0000 (Coordinated Universal Time)
---

## Introduction

This integration between Adobe Campaign v8 and Adobe Experience Manager allows you to use content created in Adobe Experience Manager in your Adobe Campaign emails.

[]()

To help you demonstrate this integration, we have pre-configured the following in AEM CS and Campaign v8 in the ***Adobe Demo System Shared**** *organization:&#x20;

> ✔️ Campaign v8: AEM External Account

> ✔️ AEM CS: Campaign v8 Cloud Service

> ✔️ AEM CS: New Email Template

> ✔️ Campaign v8: New AEM Email Template

:::hint{type="warning"}
The AEM sandbox **Adobe Demo System Shared Program 1** is used only to demonstrate Journey Optimizer and Campaign v8 Email template integration with AEM Cloud Services. Please do not create custom demos for other purposes in this shared environment.
:::



## How do you demonstrate AEM Email template integration with Campaign?

Let's explore in detail what you can demonstrate in each solution.

### AEM Cloud Services details

In AEM CS, the following email templates have been pre-configured:

[**Luma - Welcome Email AEM template link**](https://author-p97303-e890303.adobeaemcloud.com/ui#/aem/editor.html/content/campaigns/luma/master/luma-campaigns/luma---welcome-email.html?appId=aemshell)

![](../../assets/seYAhJ7vRse8uH0d3CqR2_cleanshot-2024-08-22-at-152341-2x.png)

[SecurFinancial - Welcome Email AEM template](https://author-p97303-e890303.adobeaemcloud.com/ui#/aem/editor.html/content/campaigns/luma/master/luma-campaigns/securfinancial---welcome-email.html?appId=aemshell)



![](../../assets/VRe6IqtzTyi74v_0f4fIm_cleanshot-2024-08-30-at-153819-2x.png)



These email templates have been **approved** and can be synced with an Adobe Campaign email delivery.



### Campaign v8 Web UI details

Below are the steps to create a Campaign email delivery and select an AEM Email template:

1. Navigate to [Campaign v8 Home](https://experience.adobe.com/#/@demosystem4/so\:demosystem4-mkt-prod1/acc/home)
2. Click on Campaign Management >** Deliveries**
3. Click on the button **Create delivery**
4. Select the Email channel, then select the email template: **Email delivery with AEM Content, **then click on the **Confirm** button.
5. Click on **Create delivery**
6. In the **Content** section, click on the button **Edit content**
7. In the **Email content** section, click on the button **Select AEM Content**
8. Remove the filter: Links: Not Linked and select Luma or SecurFinancial AEM Email Template
9. Click on the **confirm button**
10. Click on the** Save **button

You can continue by simulating content and sending proof to your test profile.

![AEM Content in a Campaign delivery](../../assets/7621qyquUe6N9NxAmG1qE_cleanshot-2024-08-30-at-154540-2x.png "AEM Content in a Campaign delivery")

![Retail - Luma AEM email template example](../../assets/dLvg8GADSIiMknGEJPBuy_cleanshot-2024-08-22-at-153245-2x.png "Retail - Luma AEM email template example")











