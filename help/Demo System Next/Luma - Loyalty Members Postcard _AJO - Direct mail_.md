---
title: Luma - Loyalty Members Postcard (AJO - Direct mail)
slug: kMQy-luma
createdAt: Mon May 27 2024 07:19:01 GMT+0000 (Coordinated Universal Time)
updatedAt: Tue May 28 2024 10:30:30 GMT+0000 (Coordinated Universal Time)
---

# Introduction

Direct mail is an offline channel that allows you to personalize and generate the extraction files required by direct mail providers to send mail to your customers.&#x20;

When creating a direct mail campaign, Journey Optimizer automatically generates a file containing all the targeted profiles and selected data, such as postal addresses and profile attributes. This file is sent to the server of your choice so that it is accessible by your chosen direct mail provider, who will handle the actual mailing process for you.

## Setup & Pre-requisities&#x20;

For the **Luma Public project**, we have set up Direct mail on **Adobe Demo System Shared - Public Project Luma** sandbox. [Click here](https://experience.adobe.com/#/@demosystem4/sname\:public-luma/journey-optimizer/campaigns/delivery/80ccc6ae-d7c6-44f1-848b-4532fed0b7ba) to check out the direct mail.

### Pre-requisite Configurations&#x20;

1. **File Routing with S3: **We have configured a dedicated AWS S3 for the Direct mail files, which will be generated from this sandbox to showcase the capability to share with direct mail vendors.

&#x20;     &#x20;

![](../../assets/GRbQ7hle_yBUUVA1u9JsW_screenshot-2024-05-27-at-125941-pm.png)

&#x20; 2\. **Channel Surface: **We have configured a channel surface to showcase the AJO direct mail channel's direct mail capability.



![](../../assets/GciFw7ycIaOChGghCUp6z_screenshot-2024-05-27-at-23635-pm.png)

### Demo - Storyline

Please take note of the following information:

For the Luma Public Project, we will be sending a postcard with offers to all Loyalty members who fall into the following tiers: Platinum, Gold, Silver, and Blue. We have created an audience for this demonstration scenario - "Luma - Loyalty Members with Address."

The audience will segment all users based on the above criteria and is batch in nature. We will utilize this audience in the AJO Campaign.

For demonstration purposes, we will have two versions of the campaign. The first version has already been executed and its output file is in S3. The second version is in draft mode and is intended to showcase the formatting of the output file and the setup of AJO direct mail campaign capability.

### **STEPS:**

Please remember the following instructions:

1\.  Go to the Adobe Demo System Shared - Public Project Luma sandbox and navigate to the campaigns section.
2\.  Click on "Create New Campaign" and provide a name with your LDAP. Then, select the audience that you have built in the previous step.
3\.  Click on "Action," select "Direct Mail," choose the surface mentioned above, and activate manually and once.
4\.  For the content, add the columns below to fetch values from the database for the profiles. Also, please ensure to tick the checkbox for timestamp addition in the filename.
5\.  Review the fields using content simulate and test profiles.
6\.  Review the campaign and then activate it. You will see your file in S3.

### Content Fields:

**Address :**

{{profile.homeAddress.street1}}{{profile.homeAddress.street2}}{{profile.homeAddress.street3}}{{profile.homeAddress.street4}}

**Zip : **{{profile.homeAddress.postalCode}}

**City : **{{profile.homeAddress.city}}

**State :**

{%#if profile.homeAddress.state.isNotNull()%} {{profile.homeAddress.state}} {%else if profile.homeAddress.stateProvince.isNotNull()%} {{profile.homeAddress.stateProvince}} {%else%} NA {%/if%}

**Loyalty Tier : **{{profile.loyalty.tier}}

**Image :**

{%#if profile.loyalty.tier.equals("gold",false)%} https\://demo-system-next.s3.amazonaws.com/assets/luma/gold-loyals-banner.jpg {%/if%}{%#if profile.loyalty.tier.equals("platinum",false)%} https\://demo-system-next.s3.amazonaws.com/assets/luma/platinum-loyals-banner.jpg {%/if%}{%#if profile.loyalty.tier.equals("silver",false)%} https\://demo-system-next.s3.amazonaws.com/assets/luma/silver-loyals-banner.jpg {%/if%}{%#if profile.loyalty.tier.equals("blue",false)%} https\://demo-system-next.s3.amazonaws.com/assets/luma/blue-loyals-free-shipping.jpg{%/if%}



