---
title: Set up journeys and messages on your sandbox
slug: qkvW-set-up-journeys-and-messages-on-your-sandbox
createdAt: Mon Oct 07 2024 06:37:20 GMT+0000 (Coordinated Universal Time)
updatedAt: Mon Oct 07 2024 06:44:46 GMT+0000 (Coordinated Universal Time)
---

## **Goal:**

This scenario will create sample journeys/messages on the fly from Dashboard. We are importing below mentioned journeys on the sandbox which you have selected in the dashboard.

- Retail Journeys - Selecting this option provides sample web and mobile journeys on the selected sandbox
  - &#x20;Web Journeys: Learn more
  - &#x20;Mobile Journeys: Learn More
- Media & Entertainment - Selecting this option will provide content for User Registration - Sample Journey that will send a welcome email after the user has logged in on the webpage
- Automotive - Selecting this option will provide content for User Registration - Sample Journey that will send a welcome email after the user has logged in on the webpage
- Telco verticals - Selecting this option will provide content for User Registration - Sample Journey that will send a welcome email after the user has logged in on the webpage
- Mobile Push Notifications - This will provide sample mobile push journey

## **Before you begin:**

1. AJO should be configured on the sandbox with **"Transactional Preset**" for sending email messages and **"Push Preset" **for sending mobile push notifications.
2. There are some journey's and message's which are using **segments and offers**, if these offers/decisions are not present, there will be error while publishing the message's and journey's linked to them.
3. Your IMS Org is enabled for journey import/export API's. Reach out to us if you are not aware of it
4. For installing schemas/offers/segments use [Quick Setup](https://dsn.adobe.com/quick-setup).
5. Messages linked to "**Luma Website Checkout Abandoners**", "**Luma - Website - Purchase Confirmation**", "**Luma - Back in Stock Alert**"  uses journey event Id's. Right now, we are unable to automate this part due to limitation in journey's API. Please follow below mentioned steps to manually update the event Id in the messages.

## How to set up?&#x20;

1. Go to [Quick Setup](https://dsn.adobe.com/quick-setup).
2. Selected Preset Journey's should be installed on the sandbox.

## Due to Journey API's Limitation, please update below steps manually

**WEB:** &#x20;

Follow link to update journeys and messages

Publishing the journeys is a manual step right now, please publish all the journeys created by DSN quick setup

**MOBILE:**

Please make sure to set up journey optimiser for push notification: Configuration

Update the "BRANDNAME" with the project ID, you are using for the demo. This is required so that push can be sent to the project are demonstrating to your customer

![](https://docs.adobedemo.com/~gitbook/image?url=https%3A%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MMLrO7TweNFMn8PgeVh%252Fuploads%252Fws7d3tq49GCjIcmcDDlv%252FScreenshot%25202022-02-10%2520at%25207.16.23%2520PM.png%3Falt%3Dmedia%26token%3D4196c133-f601-4c21-8bc5-a62ee66dfde5\&width=768\&dpr=4\&quality=100\&sign=80bc07e3\&sv=1)

![](https://docs.adobedemo.com/~gitbook/image?url=https%3A%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MMLrO7TweNFMn8PgeVh%252Fuploads%252F63lsGDXDJKX6SdnX7HYw%252FScreenshot%25202022-02-10%2520at%25207.18.34%2520PM.png%3Falt%3Dmedia%26token%3D2aed576c-191f-40d0-ba62-b3ab326429b2\&width=768\&dpr=4\&quality=100\&sign=9dd38722\&sv=1)





