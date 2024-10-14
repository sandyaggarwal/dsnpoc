---
title: AJO Mobile In-App Message
slug: JjvM-mobile
createdAt: Tue May 14 2024 07:43:19 GMT+0000 (Coordinated Universal Time)
updatedAt: Tue Jun 18 2024 08:13:43 GMT+0000 (Coordinated Universal Time)
---

An AJO Mobile in-app message is a concise notification or announcement that appears within the AJO Mobile application. These messages commonly relay updates, introduce new features, announce promotions, or share crucial app-related information. Their primary objective is to captivate users' attention and motivate them to undertake specific actions, like updating the app to unlock new features or joining promotional activities.

### Prerequistes

1. Ensure you have the latest DSN schemas and a vertical mobile app set up.
2. Within AEP Data Collection, edit the mobile datastream to include **Offer Decisioning **and **Adobe Journey Optimizer.**

   ![](../../assets/UT-vLAPTR987bg5-KCN74_image.png)

3.In Adobe Experience Platform, make sure you have the default merge policy with the **Active-On-Edge Merge Policy** option enabled. To do this, select a policy under the **Customer** > **Profiles** > **Merge Policies** Experience Platform menu.



![](../../assets/L_xvjRFJPWhsNSrJcIzb6_image.png)

## Channel configuration prerequisites

**Configue App Surface - **<https://dsn.adobe.com/docs/configure-app-surface>

### Create an In-app message

1. Go to AJO. Access the **Campaigns** menu, then click **Create campaign**.
2. In the Properties section, select when the campaign execution type: Scheduled or API-triggered. Select Scheduled.
3. &#x20;In the Actions section, choose the In-app message and the App surface previously configured for your In-app message. (If you don't have any app surfaces follow this link <https://dsn.adobe.com/docs/configure-app-surface>).Then, click Create.



![](../../assets/9sxMDcpSfxSU20vNgPq7N_image.png)



4.In the **Properties** section, enter the **Title** and the **Description** description.



![](../../assets/X9iaU3agD4LhPRJZoiI92_image.png)

5.Click **Edit triggers **to choose the event(s) and criteria that will trigger your message. Rule builders enable users to specify criteria and values that, when met, trigger a set of actions, such as sending an in-app message.

a.Click the event drop-down to change the Trigger if needed.



![](../../assets/dgdUAdw4qw6jJI7daWw6t_image.png)



b.Click **Add condition** if you want the trigger to consider multiple events or criteria.

c.Choose the **Or** condition if you want to add more **Triggers** to further expand the rule.

d.Click Done.

![](../../assets/4heIUtwcT-tzoPEzQZjGf_image.png)

6.Click Edit content to design the content.

a.Provide Media, Content and button details.

![](../../assets/IlMbkVvWRwwlI6SEK_SM4_image.png)

7.Click Review to activate.

8\. Open the app, In-app message will be displayed on app launch.

### How to send custom events from mobile app to platform?

1. Open builder interface. Go to project and navigate to any screen in mobile project.This will open the sidebar.



![](../../assets/qwg-6px6iP-xlxEx95YFA_screenshot-2024-06-03-at-32857-pm.png)

2.Click on Events. You can send any event by selecting it in dropdown. If Custom Event is selected, provide a value for custom event.



![](../../assets/yloA1UAuDdGS8kk1SIqUh_image.png)

3\. You can also use button component to send an event to platform. Click on Edit Content.&#x20;

Add a button component and select event type in dropdown.



![](../../assets/R4NCxb7qPNynUN_r3CxMN_image.png)

Demo Scenario to show In-App mesage in DSN public projects:



- Luma [In-app support](<../Demo System Next/In-app support.md>) demo description
- Frescopca [In-app support](<../Demo System Next/In-app support.md>) demo description

