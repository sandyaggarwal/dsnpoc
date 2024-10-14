---
title: AJO Web In-App message
slug: E9Qy-web-in-app
createdAt: Thu Apr 11 2024 11:57:55 GMT+0000 (Coordinated Universal Time)
updatedAt: Tue Jun 18 2024 07:30:10 GMT+0000 (Coordinated Universal Time)
---

AJO web in-app messages are notifications or announcements visible within the AJO web application. Much like their mobile counterparts, these messages inform users about updates, new features, promotions, or pertinent information concerning the web application. They aim to engage users and prompt them to take actions like exploring new features or participating in promotions, all directly within the web application.

## High-Level Instructions

1. Ensure you have the latest DSN schemas and a vertical website set up, such as Luma.
2. With AEP Data Collection, edit the website datastream to include **Offer Decisioning **and **Adobe Journey Optimizer.**
3. Create the new in-app campaign in AJO and specify the base URL, such as **dsn.adobe.com/web/abc-1234**&#x20;
4. Set the triggering criteria to: (Sent data to Platform event happens) AND (XDM event type is web.webpagedetails.pageViews)
5. Activate the campaign. It will take a few minutes, but the in-app message should start appearing. Start the user experience with the exact URL that matches the base URL. For example, **dsn.adobe.com/web/abc-1234 **rather than **dsn.adobe.com/web/abc-1234/home**



## To trigger on just a specific page

Follow the steps above, but in step 4, add a third limiting factor, such as page name. For example, the full triggering criteria could look like:&#x20;

**(Sent data to Platform event happens) AND (XDM event type is web.webpagedetails.pageViews) AND (XDM value web.webPageDetails.name = gear)**



## Step-by-step guide

Below are the steps to implement AJO Web in-app messages using Demo System Next web projects.



- 1\. Create a new Luma web project using the Quick Setup and selecting the **Luma - Basic** preset
-

  ![](../../assets/3DiqcRAulhjZ9cJA8_qVK_cleanshot-2024-04-11-at-143657.png)

* 2\. Open the Home menu of your Experience Platform sandbox and navigate to Datastreams. Edit the Service **Adobe Experience Platform,** check **Offer Decisioning **and **Adobe Journey Optimizer, **and then Save.
*

  ![](../../assets/5mpAUNKmM3SQmZ76LtAMs_cleanshot-2024-04-11-at-140953.png)

- 3\. Navigate to Journey Optimizer using the solution switch (top right) and create a new Web In-app message Campaign. In the app surface, enter **dsn.adobe.com/web/abc-1234**. Click **Create**
-

  ![](../../assets/cgBOhA7zqV3L2voAWT3o7_cleanshot-2024-04-11-at-141323.png)

* 4\. In the Audience section, enter a name, e.g., Sample In-App Flash Sale, and keep it for all app users using the ECID identity type. Keep the **Action** set to the same URL as the base URL.&#x20;

  Edit the **Triggers**, set the Show message If as the following:&#x20;

  (Sent data to Platform event happens) AND (XDM event type is web.webpagedetails.pageViews) AND (XDM Value web.webpagedetails.name equals gear)


*

  ![](../../assets/HA1iQXqWz2K3vW8eOIw7X_cleanshot-2024-04-11-at-142638.png)

- 5\. Edit your in-app message content by adding the **Media URL**, **Header**, **Body**, **Buttons, **and the select a **Message Layout**


-

  ![](../../assets/Lrx87gcKB0if_GMGjUo_b_cleanshot-2024-04-11-at-142942.png)

* 5\. Edit your in-app message content by adding the **Media URL**, **Header**, **Body**, **Buttons, **and the select a **Message Layout**. Click on **Review to Activate**.&#x20;

  **Note***: It may take a few minutes to be activated.*


*

  ![](../../assets/Lrx87gcKB0if_GMGjUo_b_cleanshot-2024-04-11-at-142942.png)

- 6\. Open your DSN Luma Web project, e.g. **dsn.adobe.com/web/abc-1234**, and navigate to the **Gear** page; you should see the in-app message.
-

  ![](../../assets/HUHlHIz7afERDhwqLa9Ct_cleanshot-2024-04-11-at-143450.png)

### Demo Scenario to show In-App mesage in DSN public projects:



- Luma [In-app support](<../Demo System Next/In-app support.md>) demo description
- Frescopca [In-app support](<../Demo System Next/In-app support.md>) demo description

