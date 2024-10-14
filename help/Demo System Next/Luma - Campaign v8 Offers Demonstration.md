---
title: Luma - Campaign v8 Offers Demonstration
slug: w6CW-luma
createdAt: Thu Aug 29 2024 19:15:02 GMT+0000 (Coordinated Universal Time)
updatedAt: Fri Aug 30 2024 10:27:42 GMT+0000 (Coordinated Universal Time)
---

# Introduction

The primary objective is to showcase the offer or coupon management capability based on various customer attributes and actions of the Luma retail brand.

## Environment

We will utilize the[ Adobe](https://experience.adobe.com/#/@demosystem4/so\:demosystem4-mkt-prod1/acc/home)[** Demo System Shared Campaign v8 Sandbox**](https://experience.adobe.com/#/@demosystem4/so\:demosystem4-mkt-prod1/acc/home) for this Luma Offer Demonstration.

## Configurations

We have dedicated Offer Space and Catalog for the Luma brand in Campaign v8.

### &#x20;Offer Space&#x20;

We have a dedicated folder structure for the Luma Retail brand and categories. Currently, we support **Email, Direct Mail**, and **Web** offer spaces for Luma.&#x20;

![](../../assets/dQLi-Z3d54IWBOHXQHCYs_screenshot-2024-08-30-at-125333-am.png)

### Offers

Based on different interests and attributes, we have created offers for Luma.

**Interests:**

1. Interested in Gyming.
2. Interested in Yoga.
3. Interested in Cycling.
4. Interested in Hiking.
5. Interested in Running&#x20;
6. Interested in Men's Athleisure.
7. Interested in Women's Athleisure.
8. Interested in Equipments.

**Loyalty Status(Luma +):**

1. Blue Members
2. Silver Members
3. Gold Members
4. Platinum Members.

### Recipients

A  dedicated recipient folder ([Luma Recipients](https://experience.adobe.com/#/@demosystem4/so\:demosystem4-mkt-prod1/acc/folders/folder/119982/nmsRecipient)) with the recipient's data including fields that we will utilize for offer eligibility in the offer's query tab.

![](../../assets/tLnKXajDoVbS1BlZZod03_screenshot-2024-08-30-at-11001-am.png)

### Delivery Template and Personalization Block

We have created a dedicated email template ([Luma Interests & Offer Email](https://experience.adobe.com/#/@demosystem4/so\:demosystem4-mkt-prod1/acc/folders/folder/1186/nmsDelivery/123194)) with a **personalization block** to include the qualifying offer for the recipient to quickly demonstrate the look of the offer in the email.

![](../../assets/PJ1eUm33BpVQ2fB8bORpu_screenshot-2024-08-30-at-15037-am.png)

## Modifying Recipients Interest

1. Go to [Adobe Campaign](https://experience.adobe.com/#/@demosystem4/so\:demosystem4-mkt-prod1/acc/home) from the left panel and click on **Explorer**.
2. Go to **Global > Profiles & Target > Recipient > Luma Recipient.**
3. Click on any recipient and make a note of the profile **email id.**
4. Then a form will appear and you can update the profile interest accordingly under **custom fields** and click on **save**.

![](../../assets/jVG5akImcaSU1Ai5v-XmN_screenshot-2024-08-30-at-14111-am.png)

## Offer Eligibility & Criteria

Offer eligibility depends on various **criteria**:

1. A Luma customer.
2. A Luma customer with membership.
3. A Luma customer with interests.
4. A Luma customer with membership and interests.

**Eligibility Scenario**:

1. A Luma customer with **no membership** and** no interests** is eligible to receive a Join Luma + offer.
2. A Luma customer with **membership** and **no interests** is eligible to receive a corresponding Luma + status offer.
3. A Luma customer with **no membership** and **have interests** is eligible to receive a corresponding Luma interest offer.
4. A Luma customer with **membership** and **interests** is eligible to receive a corresponding Luma interest offer.

So, the **highest precedence** is for Interest Offers rather than membership or fallback offer.&#x20;

Also, for each interest offer we have defined weightage if they are a member then the weight will be high or else low.

![](../../assets/1saBJrbIsfGFQEWUSDZDd_screenshot-2024-08-30-at-13311-am.png)

## Preview Offer in Email Delivery

### STEPS:

1. Go to Adobe Campaign from the left panel and click on **Deliveries**.&#x20;

![](../../assets/1UtkD9OLNRdBktcDdrzQE_screenshot-2024-08-30-at-33320-pm.png)

2\. Click on **Create Delivery **and select Channel **email** and in the **drop-down** select the **Luma Interests & Offer** Email delivery template.

![](../../assets/ixiHtqaL-IZ7DI-pdm6-V_screenshot-2024-08-30-at-33657-pm.png)

![](../../assets/uFtcaNVnHQhDVpJoVbCA8_screenshot-2024-08-30-at-33745-pm.png)

3\. Click on **Create Delivery **and you will **edit content** and edit the **email body,** Check that there is an **Offer personalization block** at the bottom before the footer.

![](../../assets/-TjXO26FxUw_VXYLPHMEJ_screenshot-2024-08-30-at-33846-pm.png)

4\. Then go to **simulate content **and from the panel click on **add test profile**.

![](../../assets/LLEc2jOBPvfWLJmIh5Bck_screenshot-2024-08-30-at-34005-pm.png)

5\. Then go to the **Profiles tab** and search with your **noted email id.**

![](../../assets/nAkqsC5dN54KuwE_yalaU_screenshot-2024-08-30-at-34107-pm.png)

6\.  Let the content load and you will see the offer rendering for the **recipient**.

![](../../assets/RtLuL8qu_KFjvwtmiwG8a_screenshot-2024-08-30-at-34152-pm.png)

