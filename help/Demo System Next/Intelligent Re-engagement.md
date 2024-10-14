---
title: Intelligent Re-engagement
slug: cl8P-intelligent-re-engagement
createdAt: Wed Apr 17 2024 17:00:57 GMT+0000 (Coordinated Universal Time)
updatedAt: Tue May 07 2024 14:46:51 GMT+0000 (Coordinated Universal Time)
---

### Business Objectives

Beth is a customer at a large national retailer, Luma. While Beth has an Luma account, she’s been a sporadic buyer over the years. In the past, it’s been difficult for Luma to understand and act on Beth’s buying patterns well enough to turn her into a loyal customer across their product categories. Luma wants to promote intelligent re-engagement with Beth to consistently deliver a compelling and connected experience in the moments that matter.&#x20;

### Persona Intro

Beth, 35-year-old woman.


### Prerequisites

Beth is an existing customer so before starting the demo, you need to prepare her profile:

1. Use registration form in Luma website to create a profile. Part of the script involves receiving SMS so phone number is an important field, make sure you enter it in this format: \<your-real-phone-number>+\<some-random-digits>. So if your real phone number is +0123456789, in registration form you should enter it as +0123456789+171101. Also make sure to select SMS as your preferred channel:

![](../../assets/KRkCsFbmRhGhLpi5DfeZl_image.png)

2\. Make a purchase - in Luma website, add any product to the cart, then checkout and place an complete the purchase.

3\. Sign in in the mobile app

### Scenario

<https://dsn.adobe.com/cx2/luma3-jt>


- One Sunday, Beth decides to go to the mall to shop for some new athletic tops. She decides to visit Luma. Beth has the Luma mobile app. Using geo-fencing capabilities, Luma captures Beth’s in-store visit as an interaction event. This event is streamed into Beth’s unified customer profile in the Real-Time CDP and simultaneously sent to Customer Journey Analytics. Beth leaves the store without making a purchase.&#x20;



  Behind the scenes, Luma set up a streaming segment in the Real-Time CDP. This segment is built to capture account holders that have visited a store within the last 24 hours but have not made a purchase: “in-store abandoners”. Beth qualifies for this segment.&#x20;



  Open 

  Search for your demo persona using email.
-

  ![](../../assets/ZE5-Yi8qnKwmtAjSs9U0S_image.png)

*





  We need to simulate in-store visit.

  Click Trigger Journey for "Store entry" and after few seconds "Store Exit" action.
*

  ![](../../assets/Crrl1iXv4KGBTHUFtmRb5_image.png)



  ![](../../assets/CAxGDwJZuDZcEGCMPPFDZ_image.png)

- Beth’s qualification for the “in-store abandoners” streaming segment automatically kicks off a journey in Adobe Journey Optimizer. To see if they can capture any other interaction events from Beth (whether online or offline) and to decrease the potential “creepiness factor”, Luma sets a condition to wait three days before contacting Beth.&#x20;
-

  ![](../../assets/zL8z_hymcM7D5xzNrsyCC_image.png)

* Without another interaction event, after 3 days (For the purpose of the demo we reduced the waiting time to 10 seconds), Luma sends a nudge communication to Beth about the new athletic tops newly in stock in her local store. AJO ensures this message is sent to one of her consented communication channels, which is noted in the “channel preferences” section of her unified customer profile. An SMS message is sent at the optimal time for Beth using the send-time optimization features in AJO. Show SMS as a channel with a check mark in Beth’s unified profile under “channel preferences”. Show SMS coming through on a mobile device with the message: “Hey Beth, check out our new athletic gear recently stocked at your local store! \[LINK]”
*

- Beth clicks the link in the SMS, which instantly brings her to the Luma app. She browses the new athletic tops on the app for about 15 minutes. She favorites a few by adding them to her wish list.&#x20;



  Highlight that certain product cards have “newly stocked” stickers and that this can be enabled by data from either streaming in from Adobe Commerce or other commerce engine (i.e. Shopify)&#x20;



  Open the mobile app either from the sms link or directly (in the second case go to women's category items). Browse few products, add some of them to the wish list by clicking the star in the top left corner. 
-

  ![](../../assets/vzA5fDSCVsRY4P00B8fc0_image.png)



  ![](../../assets/Nt25n8EyR-OqphC3EBhrK_image.png)

* All of Beth’s interaction data, including her open time, click through event, and browsing behaviour on the Luma app are streamed into her unified profile in Real-Time CDP.&#x20;



  Use Profile Viewer to show the gathered events. You can also go directly to AEP UI, into Beth’s unified profile. Show new experience events flowing in. 
*

  ![](../../assets/K4pqYr4L-bW19aQPOs-wO_image.png)

- In the background, a Customer.ai is calculating Beth’s propensity to purchase various products based on her interaction events over the last week as well as other elements in her unified profile. These propensity scores are continually updated as Beth interacts with Luma.&#x20;



  Show that the propensity score is updated in the profile attributes.
-

  ![](../../assets/GiKdPrqV_kiMh0Xc1-6Sy_image.png)

* As the new winter season approaches, the Analytics team at Luma wants to run some statistical analysis for an upcoming athleisure promotion. To do this, they want to use purchase and interaction data from prior years, combined with recent behavioral data streaming in from online and offline channels. Using CJA, Luma performs an analysis to understand the number of purchase events and in-store visits by season and which marketing channels were most effective at driving those purchase events. They overlay this analysis with a filter for the “tops” product category. They create an audience called “Winter athleisure purchases with a recent abandon event.” The Luma Analytics team immediately publishes this audience to CDP for further segment personalization and downstream activation.&#x20;
*

  ![](../../assets/15-JP_AUcxdU51XrKifMF_image.png)

- Back in CDP, the “Winter athleisure purchases with a recent abandon event” audience is used to create another audience, one that takes into account loyalty member status, propensity to purchase shoes, and recent online interaction events. They name this segment “Winter athleisure purchases with a recent abandon event but high intent to purchase.” Beth falls into this segment. Show segment builder and show construction of this new segment&#x20;



  Show Beth’s unified profile where “Winter athleisure purchases with a recent abandon event but high intent to purchase” now shows up in her segment membership&#x20;



  Use Profile Viewer to show the new segments beeing resolved
-

  ![](../../assets/Gg83h1Cmdd7K5dU22H5CS_image.png)

* The “Winter athleisure purchases with a recent abandon event but high intent to purchase” segment is also used in AJO, where Beth’s qualification for this segment kicks off the journey further.
*

- Due to email being the most effective marketing channel to drive purchases in past winter seasons, email is chosen as the next best channel for communication with Beth. Based on the new variables available, the Luma marketing team provides a completely different campaign to Beth, including modified campaign content and compelling calls to action. Show the build of an additional step in Beth’s journey in the orchestration canvas&#x20;



  Click on the action for email send, show how different variables are taken into account within email authoring&#x20;



  Show you inbox to show the email that was send with AJO. Click on the link for "Buy the look"
-

* The email includes suggested products based on the items in Beth’s wish list with a compelling call to action to see more ways the tops in her wish list could be styled. She clicks the link and is brought to the Luma website. Show email being triggered, show email and show click through event to the website.&#x20;



  Click "add to cart" on the "Buy the look" website. All items should be added to the cart.
*

- After seeing all the different ways the tops in her wish list could be styled, Beth is convinced she’ll get maximum value from them. She adds the items to her cart and makes the purchase.



  Follow the buying process to finish the purchase
-

* Immediately following her purchase event, Beth is “unsegmented” from the CDP segment “Winter athleisure purchasers with a recent abandon event but high intent to purchase.” This suppresses her from seeing additional advertisements for Luma winter athleisure tops across paid media and other channels. Show in her profile how she doesn’t qualify for this segment anymore – doesn’t show up in segment membership.
*

- Her purchase event also triggers a purchase confirmation email that is sent with AJO. Show email that gets sent using trigger from prior step.&#x20;



  Show you inbox to show the email that was send with AJO. 
-

* A few days later when Beth’s tops have shipped, she gets a push notification alerting her that her tops have shipped and an estimated ETA on the delivery date. Show push notification on mobile device.&#x20;



  You should recieve a push notification on your mobile phone with information about the shippment
*

- Following the conversion (purchase) event, the Analytics team at Luma uses Attribution IQ in CJA to determine the attribution channels that played a part in Beth’s purchase event, including the relative credit to be given to each channel based on a chosen attribution model or using an algorithmic attribution model. Luma uses this attribution data to better inform and optimize marketing campaigns, improve digital self-service capabilities to reduce call center volume, and improve personalization activities in the future. Show Attribution AI report
-

