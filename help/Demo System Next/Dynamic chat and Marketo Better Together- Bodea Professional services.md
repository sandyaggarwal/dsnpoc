---
title: Dynamic chat and Marketo Better Together- Bodea Professional services
slug: __b9-dynamic
createdAt: Mon Apr 08 2024 09:17:49 GMT+0000 (Coordinated Universal Time)
updatedAt: Tue May 14 2024 11:27:53 GMT+0000 (Coordinated Universal Time)
---

## **Introduction**

This page is a practical guide on how to run a demonstration that showcases the enhanced capabilities of Dynamic chat and Marketo when used together. The demo will illustrate how transitioning of leads to AEP.

## **Use Case**

All the leads who interact with the dynamic chat window on Bodea professional services webinar [page](https://dsn.adobe.com/web/bodea/professional-services-webinar) will be transitioning as the following: SFDC > Marketo > Dynamic Chat > Marketo > AEP (source connector).

Bodea decided to further nurture these leads through various marketing strategies in Marketo.

## **Demo Video**

Click here to check the Demo steps video. (under process)

## Step-by-step guide

| Step | Topic                                          | Instructions                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| ---- | ---------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 1    | DC on Bodea professional services webinar page | ***Prerequisite:***To populate the correct account details in B2B RT-CDP profile view and showcase the stitching between accounts and profiles, create a new contact in the shared SFDC demo instance (screen and steps below).1) Create a new contact
2) Key in any of your test id (LDAP+123\@adobetest.com)
3) Mention the company name as Adobe
4) ![](../../assets/Wq7Y0OzMVmo_ferDk0dso_image.png)***Note:*** Once you are done with the above prerequisite and ensured, that the Marketo activity log has been updated for the test ID creation (from SFDC) in Marketo, you are ready to go ahead and execute the demo by following the below steps.1) Navigate to [Bodea professional services webinar](https://dsn.adobe.com/web/bodea/professional-services-webinar) Website. We recommend you to open this website in the incognito mode of your browser, which allows you to start your session afresh.
2) Wait for 2 to 3 seconds on the page
3) DC chat pop-up appears on the page (down right)
4) Click on the **pop-up **(screen1)
5) Click on **Sign me up!** button (screen2) in the chat window and provide details like First, Last Name and Email address (use the same email created above in the pre-requisite steps in SFDC) details to register for the webinar!*Screens below:*1) ![](../../assets/Yg_Fl2g1Q0a2jasN4JGGV_image.png)
2) ![](../../assets/riozLECQvH7fCprCv91L4_image.png) |
| 2    | RTCDP lead profile                             | 1. Navigate to [Profiles](https://experience.adobe.com/#/@demosystem4/sname\:public-bodea/platform/profile/browse?limit=25\&page=1).
2. Click on Browse and search for the email ID used during Dynamic chat conversation in the above steps.
3. Click on the profile ID and check the details and attributes.
4. Click on the Events tab under the profile to see the series of events for the lead.***Note:*** There can be some latency here for the sync between Marketo and B2RT-CDP.*Screen below:*1. ![](../../assets/6HVdeiW8lAASkbkX_-3Ry_image.png)![](../../assets/5QQsuTVsWCdk8iY_TetF4_image.png)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| 3    | Marketo Engage                                 | 1) Navigate to [Marketo](https://engage-ab.marketo.com/?munchkinId=542-BPB-398#/classic/MM0A1).
2)  Click on Database (Default Workspace).
3) Search for the email ID used during Dynamic chat conversation.*Screen below:*1) ![](../../assets/rQgeRsvXRpO4lOitGHlMt_image.png)
2) Click on the person ID and go to [Activity Log](https://app-abdemo1.marketo.com/leadDatabase/loadLeadDetail?leadId=1001338\&accessZoneId=1) tab of the lead profile.
3) You will see the Activity type and details of the events that happened.*Screen below:*1) ![](../../assets/fWnq5DxzaTRYHUqeX222B_image.png)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |

## System View

![](../../assets/z6BWcpjxMn5mX1GtVaOod_image.png)

## Demo environments

- **AEP Sandbox**: [Public project - Bodea](https://experience.adobe.com/#/@demosystem4/sname\:public-bodea/platform/home)
- **Marketo**: [MKTO-542-BPB-398](https://engage-ab.marketo.com/?munchkinId=542-BPB-398#/classic/MM0A1)
- **SFDC:** [Instance details](https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=demosystem\&title=Marketo+Shared+instance+for+Adobe+Demo+System+Shared+org)

