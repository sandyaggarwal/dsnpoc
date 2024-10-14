---
title: ATM Screen - Code-based Experience
slug: QFIP-xsc-demo-script-code-based-experiences
createdAt: Fri Apr 05 2024 18:49:17 GMT+0000 (Coordinated Universal Time)
updatedAt: Fri May 03 2024 12:12:07 GMT+0000 (Coordinated Universal Time)
---

### Steps

Starting point

SecurFinancial ATM screen - <https://dsn.adobe.com/web/securfinancial-cbe>

- To set up a new experience to connect within our ATMs screens :

  *Start on home screen >>> click on Campaigns >>> click on Create campaign*
-

  ![](../../assets/LpjXuOn2zHiNyBRht_85y_screenshot-2024-04-06-at-124850-am.png)



  ![](../../assets/fh_b5Xc-_2RjZ96c6wXxL_screenshot-2024-04-06-at-124913-am.png)







- Select Code Based Experiences while creating a new Campaign. When selecting it, enter a sample URI to link to demo ATM.&#x20;

  *Click on Code-Based Experience >>> Enter the URI to link to the demo ATM screen >>> Click Create*
-

  ![](../../assets/S2vteyNFgUK5Yp8hRieFb_screenshot-2024-04-06-at-125011-am.png)

* Fill out the metadata for this campaign. Provide a simple name for this experience. Keep the audience and identity type as is. Before setting up the content, create an experiment to test between different experiences.&#x20;

  *Enter a name of “ATM Experience” >>> Click Create Experiment*
*

  ![](../../assets/blFQg4TMzW4YjdgQkkN9s_screenshot-2024-04-06-at-125807-am.png)

- Marketers have the option to define their preferred metric for success such as impressions or interactions. Keep the success metric the same and add another treatment to create a 50-50 split.&#x20;

  *Click Add Treatment >>> Click Create*
-

  ![](../../assets/XXTJx9OXHfCfmpYlmoFZ1_screenshot-2024-04-06-at-125952-am.png)

* Go ahead and add the content. Both the treatments available for editing. Start by editing Treatment A.&#x20;

  *Click Edit Content >>> Click Edit Code*
*

  ![](../../assets/0vjFs5yMuB_6zgj0Y2Y3G_screenshot-2024-04-06-at-10042-am.png)





  ![](../../assets/M8bWPlhjm0LrySQ2DE-Ii_screenshot-2024-04-06-at-10126-am.png)







- Within the editor, define the content either as HTML or as JSON. For demo purposes we will use JSON. For this demonstration, will keep the payload simple and pass only an image and text. We have full access to all the personalization options available within Adobe Journey Optimizer.&#x20;

  For this example, we will include the customer’s first name to personalize this message.&#x20;

  *Switch mode to JSON >>> Click on the screen to add in the following full code: *

  {

  "title": "SecurFinancial Bistro Banking",
  "image":"<https://demo-system-next.s3.amazonaws.com/assets/securfinancial/BistroBanking.jpeg>",
  "text":"{{profile.person.name.firstName}}, did you know SecurFinancial has Bistro Banking"
  }&#x20;

  *Click Save and close*
-

  ![](../../assets/7_WyakyJx2b1cqj3c4_El_image.png)

* Preview this experience to confirm that the personalization is working.&#x20;

  *Click on Simulate Content *
*

  ![](../../assets/7dTiJN8C5cjV_9ezeK5x0_image.png)



  ![](../../assets/wZfM-uNg3-Erh8mpuTupL_image.png)





-

  Personalize the experience for the other treatment.

  *Click on Treatment B >>> Click on Edit Code*

  Add a straightforward alternate offer of 3 monthly transactions.

  *Click on the screen to add in the following full code: *

  {

  "title":"Unlock Freedom with SecurFinancial",
  "image":"<https://demo-system-next.s3.amazonaws.com/assets/securfinancial/offers.png>",
  "text":"{{profile.person.name.firstName}}, 3 free monthly transactions, use Securfinancial ATM anywhere hassle-free!"
  }

  *Click Save and close*
-



  ![](../../assets/rGCZGo7zSJnW9izo2MEPT_image.png)



  ![](../../assets/FyyXnkqMoAlOLYE68maji_image.png)

* There is an option to schedule the start and end dates for this content is shown. In this case we are going to choose to keep this campaign active until it is manually stopped.&#x20;

  *Click Review to Activate >>> *















  *Click Activate*
*



  ![](../../assets/t8GjZaROd6F5OwrxM2zVh_image.png)



  ![](../../assets/1tj8rCoQf47De3lQJCShs_image.png)

  ![](../../assets/hH3IWMNhbs7_JXVgC7NJa_image.png)







- With this experience now activated, we can transition over to our demo [ATM screen](https://dsn.adobe.com/web/securfinancial-cbe).&#x20;

  Our customer, Bobby, will either see the bistro messaging or the message for 3 free monthly transactions. All impressions and interactions are recorded and viewable within the reporting screens for Code-based experiences.&#x20;

  Marketers can easily see which treatment has a better lift, and the interactions of every customer can be used to inform the next step in their personalized customer journeys. Switch over to the [ATM screen](https://dsn.adobe.com/web/securfinancial-cbe), then click to see the alternate treatment
-

  ![](../../assets/EKXU9g5aVLe_gWfR7wPp9_image.png)



  ![](../../assets/zcZvZzLdqAHSAuuzXR2wS_image.png)

