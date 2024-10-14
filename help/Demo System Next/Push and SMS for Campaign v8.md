---
title: Push and SMS for Campaign v8
slug: uNtk-cam
createdAt: Wed May 22 2024 09:52:03 GMT+0000 (Coordinated Universal Time)
updatedAt: Fri Aug 30 2024 12:31:24 GMT+0000 (Coordinated Universal Time)
---

This page explains how to utilize the Push and SMS channels in the **Adobe Demo System Shared** Campaign v8 production instance.

## How to demonstrate the Push notification channel?

### Install the DX Demo Mobile App

1. Navigate to <https://dsn.adobe.com/install>
2. Scan the QR code iOS, or Android QR code and install the mobile app on your device.
3. First Time You open the app, you will see this message.&#x20;

![](../../assets/IASu7_QIkpmlRHv9q6HiJ_image.png)

The app is signed with an official Adobe enterprise certificate but by default, iOS will not treat it as trusted. To add it to the list of trusted certificates go to:

- **Settings -> General -> Device Management -> Adobe Systems Inc.**

and click “Trust Adobe Systems Inc.” You only need to do it once on given device.&#x20;

During the first launch, you will have to sign in with your Adobe ID.



![](../../assets/mjVfajg7OGFw0-CsQaLRS_image.png)



### Register your device in Adobe Campaign v8

Below are the steps to register your device:

1. Open the DX Demo Mobile App
2. Click on **Settings**
3. Select Public Project **Luma v3 (Retail)**
4. Click on **Save**
5. Kill the app and open the Mobile app







## How to demonstrate the SMS Channel?

:::hint{type="warning"}
SMS messages are delivered by a partner vendor and charged back to Adobe.&#x20;

Please **DO NOT use it to send large Batch SMS campaigns!**
:::

### Prerequisites

You need to make sure your test Recipient is having the following configured:

1. Make sure your email address domain is set to @adobetest.com or @adobe.com. Otherwise, the typology rule will exclude your profile during the delivery analysis.
2. An SMS Phone number by applying the following pattern: **\[country-code]\[phone number] → e.g. 336XXXXXXXX**



![](../../assets/P9TblNK8rWzFbbnRAN0xH_cleanshot-2024-05-22-at-115822.png)

###

### Deliver your first SMS delivery

Please follow these steps to create and deliver your first SMS delivery:

<https://experienceleague.adobe.com/docs/campaign-web/v8/msg/sms/create-sms.html?lang=en>&#x20;
