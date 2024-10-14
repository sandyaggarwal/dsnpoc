---
title: Account Journeys
slug: EPhs-account-journeys
createdAt: Fri Aug 30 2024 10:36:46 GMT+0000 (Coordinated Universal Time)
updatedAt: Wed Sep 04 2024 11:11:37 GMT+0000 (Coordinated Universal Time)
---

Once we have a buying group outlined, we can build experiences or "journeys" to take them on. Unlike traditional marketing campaigns, AJO B2B Edition journeys are always on and listening for new people to bring into the experience.

***Note:*** Before designing the journey or while building it, please ensure that you have the data that qualifies for your journey's criteria at each stage. For the journey below, we ensured that we had the required qualifying (by State = CA/NY and Job Titles) data created in SFDC. This is because there is currently no way to test your journey for qualifiers.

![](../../assets/PxRE0y0dLf4COFeCLNDR0_image.png)

Here we are targeting Large companies interested in Bodea-Product X, and we can split up this audience to create unique experiences for the Accounts and people within.

![](../../assets/USe2bU08G17Bv6KiL72_2_image.png)

We are going to split this audience based on the location of the accounts for further journeys.

![](../../assets/rrgT7ZVV3_qUo1S8j2UTy_image.png)

For all the accounts from California, we split the accounts by people (by Titles) between Decision Maker/Product SME/Product Analyst.

![](../../assets/9YUsMk0GwHg98tYqCjCIn_image.png)

For Product SMEs, we are sending an email, since we are already hosting a roadshow about Bodea-Product X out of Marketo Engage, we can add all of our Product SMEs to that campaign.

![](../../assets/1vQKlvJSn1r246NA4WhGQ_image.png)

For product Analysts, we are sending an email to these people from Marketo.

![](../../assets/jaNgNXct5KL63RmtFmiBg_image.png)

For Decision Makers, we are sending an email from AJO B2B. This is key because you now can target and customize messaging for different roles as well as both the individual and the group

![](../../assets/8x-6vCl16zME3VxUoquIp_image.png)

We know that delivering the digital experiences needed to maintain great account engagement includes providing the right content to each person in your Account. That can be labor intensive. With Journey Optimizer B2B Edition, you can design highly personalized email experiences using drag-and-drop components, proven templates, or custom HTML, to maximize conversions for your journeys.

![](../../assets/VQyydv8VeWohqwIGNZM7N_image.png)

The editor allows you to display content and personalize messaging for each buying group member based on their role, account, product interest and more to offer a 1:1 buying experience.

![](../../assets/VjYa6vj1Zo1bTHw8E72ZW_image.png)

There are also built-in robust generative AI tools to help you develop outstanding email messaging for each buying group role.

![](../../assets/QxI3jLhns4Jwog333urP2_image.png)

Our generative AI tools don’t just help with content creation. Journey Optimizer B2B Edition can assist you in building your content, images, and even preheader directly in the editor so you can quickly design highly personalized experiences whil giving marketing the ability *to approve content to keep messaging and personalization aligned with brand guidelines.*

![](../../assets/uguiI_Y59aABCvQvCnywm_image.png)

The result is richer, more personalized email experiences that are quick to build and deliver to our audiences whether that be to your buyer group, individuals in the buying group, or across many accounts.

![](../../assets/mk-LW0ocmb02o5gYJ6Lx5_image.png)

Now that all of my people split have a deliverable, I close my split, wait for them to respond to one of my campaigns, and listen for their Person score to change.

![](../../assets/iwOxzMFClktozTDcSPLsz_image.png)

Now, going back to the New York track of the Journey (screen below) and adding all these people (where People's Job Title starts with C as Decision Maker) to the Buiyng group with Bodea-Product X as Solution interest and Role as Decision Maker, for all the Qualified NY accounts.

![](../../assets/J0FfLnRLavSZ8bdn_K5Jb_image.png)

We can merge these separate tracks (California and New York) at whichever point in the journey we choose.

![](../../assets/K6Djzxk0QibbuTP3U9bj5_image.png)

we can check to see which accounts within our targeted accounts are engaged (by the engagement score of the BG the account belongs to) and which accounts have not reached the level of engagement. The Buying group's status of any accounts (having an engagement score of more than 80) will be updated with Status='Engaged' to show sales readiness.

![](../../assets/bXlyZb-aiAvacaEkEkcs0_image.png)

&#x20;Also, the Account's interesting moment will be updated with Milestone='Engaged for Bodea Product x' details to show sales readiness. These accounts are now ready for sales outreach.

![](../../assets/74eSuQpVWxYf3oyvMFw0K_image.png)

***Note:**** For example, the people's score increases when they click the emails in the journey. However, the person's score would increase the engagement score of the account the person belongs to?*

*Adobe Journey Optimizer B2B calculates a buying group's engagement score by using a weighting system for each role in the group. Set the Weighting for the role, which is used to calculate the engagement score.
The value for each option is translated to a percentage for the score calculation\:Trivial = 20, Minor = 40, Normal = 60, Important = 80, and Vital = 100.
For example, a role template with roles using Vital, Important, and Normal, are then converted as 100/240, 80/240, 60/240.*

*See the below url for more details: *[*https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/buying-groups/buying-groups-role-templates*](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/buying-groups/buying-groups-role-templates)* *

Once the build is complete for the journey and ensured you have qualifiers, publish the journey for execution.
