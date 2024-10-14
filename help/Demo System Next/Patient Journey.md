---
title: Patient Journey
slug: lJ-1-p
createdAt: Thu Jun 20 2024 14:19:03 GMT+0000 (Coordinated Universal Time)
updatedAt: Thu Jun 20 2024 14:26:37 GMT+0000 (Coordinated Universal Time)
---

You can demonstrate sample journey of a patient by using the Event Trigger app for we.Healthcare.

This scenario is using we.Healthcare Patient Journey available here:<https://experience.adobe.com/#/@demosystem4/sname:public-we-healthcare/journey-optimizer/journeys/journey/670671a9-5512-4971-b179-b874d25d7563>



### Prerequisits:

The profile needs to exists in AEP and it should have email

You need to login in the mobile app with the same profile.&#x20;



![](../../assets/8REGO4rL11nf8jCd9H7v8_image.png)

### Starting Point:

<https://dsn.adobe.com/cx2/we.healthcare-jt>

### Scenario:

- Load the patient profile in the Event Trigger app by typing an id e.g. Email
-

  ![](../../assets/QpzS_jag37RROU6sVCq5G_image.png)

* After succesfull search the website will look like this&#x20;
*

  ![](../../assets/mPnveQsD90NjMTfNQGXil_image.png)

- Click "Schedule a doctor appointment" button to trigger a journey that will send an email and push notification&#x20;
-

  ![](../../assets/1qYqAtbaOfKniq50zwg47_image.png)

* Trigger the "Arriving to the medical facility" action. You should get a relevant push message.
*

  ![](../../assets/lnfXOGrd3_n-14S6fvRWD_image.png)

- Trigger the "After visit - summary" action. Another push will be delivered to your device.
-

  ![](../../assets/3QQDBW00aNEYYTwr51roS_image.png)



