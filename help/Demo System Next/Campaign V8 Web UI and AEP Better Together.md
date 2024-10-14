---
title: Campaign V8 Web UI and AEP Better Together
slug: 83_--v2
createdAt: Fri Mar 08 2024 11:11:02 GMT+0000 (Coordinated Universal Time)
updatedAt: Thu Jul 11 2024 08:08:56 GMT+0000 (Coordinated Universal Time)
---

# Introduction

This page is a practical guide on how to run a demonstration that showcases the enhanced capabilities of Adobe Campaign V8 Web User Interface and Adobe Experience Platform (AEP) when used together. The demo will illustrate how to share AEP segments with Campaign and utilize new Campaign features such as Gen AI and Asset Essentials in the email designer.

## Use Case

We will target all customers with high propensity scores and web views for Luma Yoga wear. Customers will land in the campaign web UI from AEP, where all the evaluation and eligibility are checked and shared to campaign v8 through a destination connector.

Luma decided to email these customers and inform them about the new Yoga wear launched for Luma. In campaign v8, we created a new campaign with a template to target these users. We will be using the Gen AI feature available in the email designer.

## Demo Video

**Click here** to check the Demo steps video.

## Step-by-step guide

| Step | Topic                                                      | Instructions                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| ---- | ---------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1    | AEP Web SDK                                                | 1. Navigate to [the Luma](https://dsn.adobe.com/web/luma3) Website
2. Browse **Yoga** Products
3. Click on the button **Sign in** (top right)
4. Click on the **Create an Account **button.
5. Fill out the registration form
6. Display the Segment qualification to **Luma - High Yoga Propensity Score with recent web views.**
7. **Sign in** after 1-2 minutes                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 2    | RTCDP Segmentation                                         | 1) Navigate to [Audiences](https://experience.adobe.com/#/@demosystem4/sname\:public-luma/platform/segment).
2) You can check for an audience **High Yoga Propensity Score with recent web views**.
3) It has already been activated for the Campaign v8 destination.(It runs every 3 hours to send an eligible audience in the segment to the campaign.)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| 3    | Campaign v8 - Web UI                                       | 1. Navigate to [Audience](https://experience.adobe.com/#/@demosystem4/so\:demosystem4-mkt-prod1/acc/nmsGroup).
2. See the AEP **High Yoga Propensity Score with recent web views **audience.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 4    | Campaign v8 - Campaign & Workflow creation                 | 1) Go to [Campaigns](https://experience.adobe.com/#/@demosystem4/so\:demosystem4-mkt-prod1/acc/nmsProgram).
2) Create a new Campaign.
3) Create a new campaign using the **Luma Yoga Promotions** template**.**
4) Click and open the workflow, and you will see that a few activities have already been configured. First activity is the audience which we have received from AEP i.e. Luma - High Yoga Propensity Score with recent web views - we have used a query activity go and select audience again. Second activity is a split which check's your **testing id ldap** as its a shared environment(Please edit ldap in workflow to target only desired audience.) and last activity is email communication.
5) Go to [profiles](https://experience.adobe.com/#/@demosystem4/so\:demosystem4-mkt-prod1/acc/nmsRecipient) in Adobe Campaign Web UI and **create a profile **with the same testing email ID that was used on the** **Luma website.                                                                                                                                                                                                                                                                                                             |
| 5.   | Campaign v8 - Email Creation, Asset Essentials, and Gen AI | 1.  Click and open the email activity, click on Edit Content, then Edit email body.
2. Select the **Luma features** sample template, then click on **Use this template. **
3. Click on the **main banner image** a **pop up** will be displayed select **asset essentials**(logo with image).&#x20;
4. Asset essentials pop displayed, and **click on search** and type **Luma.  **
5. **Select the image** with name : **luma-emailimageleft.jpeg** and click on **select. **
6. Now **select the text component** in the email with **New athletic gear for this summer** and **delete it**.&#x20;
7. Now **click on 2 stars** logo on the top right (Gen AI Logo). Gen AI dialogue box appears.&#x20;
8. Now under **prompt write Text for fresh yoga wear** and **click generate**.&#x20;
9. You will **see 2 to 3 variations generated** by Gen AI for the email content with topic you mentioned in prompt.&#x20;
10. **Select 1 of the variation** by clicking on **apply **and save the email.&#x20;
11. Click on **subject line** for the email and then click on **search **and type first, select the recipient firstname.&#x20;
12. Add the subject line : Check out the new Luma Yoga Collection! After the recipient's first name, then, click on save. |
| 6.   | Campaign v8 - Email Reporting                              | 1) Open the [email delivery report](https://experience.adobe.com/#/@demosystem4/so\:demosystem4-mkt-prod1/acc/nmsDelivery/55450/reports/email/sending_summary) linked to the Luma Promotional campaign.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 7.   | RTCDP - Send & Tracking Logs Profile Synchronization       | 1. Go to [Real-time CDP](https://experience.adobe.com/#/@demosystem4/sname\:public-luma/platform/home).
2. Open [Reina Retail](https://experience.adobe.com/#/@demosystem4/sname\:public-luma/platform/profile/browse/BVpqCwhy8a3op2vq3rWopf63rWopfnKJgA) golden profile
3. Show Profile attributes (Retail) and captured Experience events.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |

## System View

![](../../assets/9xeUXqU5VPSvsTFrmMfeF_systemview.png)

## Demo environments

- **AEP Sandbox**: [Public project - Luma](https://experience.adobe.com/#/@demosystem4/sname\:public-luma/platform/home)
- **Campaign v8 Web UI**: [demosystem4-mkt-prod1](https://experience.adobe.com/#/@demosystem4/so\:demosystem4-mkt-prod1/acc)



