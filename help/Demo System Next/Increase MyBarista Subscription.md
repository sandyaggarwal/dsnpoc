---
title: Increase MyBarista Subscription
slug: aXP--increase-mybarista-subscription
createdAt: Fri Dec 01 2023 09:56:44 GMT+0000 (Coordinated Universal Time)
updatedAt: Fri Dec 01 2023 10:10:49 GMT+0000 (Coordinated Universal Time)
---

### **Business Objectives**

It is a high priority for Frescopa to provide a great customer experience. Important role in their strategy playing advisors, who are helping customers with  some tasks e.g. with subscription process and take care of after sales support.&#x20;

The Fréscopa marketing team plans to:

1\) Create a campaign for the MyBarista personalized coffee subscription service.

2\) Launch a new product - Morning Muse.

3\) And create a quiz that will help customers identify their coffee profiles, providing a value exchange for 1st party data that will drive leads towards the subscription service.

### **Persona Intro**

Lizzie Torres is 22 years old single women living in New York. She is a new Fréscopa customer, she has just bought an automatic espresso machine for her home. As part of the machine’s setup, she downloads the Fréscopa mobile app, logs in, and pairs her phone to her new smart coffee machine. Lizzie falls into an audience that Fréscopa wants to target: Smart Machine users who haven’t yet subscribed to Fréscopa’s MyBarista service.

### **Prerequisites**

- Create a new demo profile (Lizzie Torres) by registering on the web page

1. &#x20;Go to [https://dsn.adobe.com/web/frescopa/register ](https://dsn.adobe.com/web/frescopa/register)and create a new profile. Make sure the answer to: Do you already have Frescopa Smart Machine is yes. After registration clean your cookies or start a new incognito session.&#x20;

![](../../assets/OQvj74pwJEgwsXis9ZnQl_image.png)

- Connect to the Frescopa project in the mobile app and log in with Lizzie's profile
  - &#x20;Open the <https://dsn.adobe.com/install> and switch to Frescopa public project from the settings screen

![](../../assets/pIk8IkGXsRrEsyE_n7Aym_image.png)

- Sign in with the demo persona email address created on the web page. Password doesn't matter. Make sure the profile is correctly loaded and merged in profile viewer (swipe from left to right)

![](../../assets/1reKRr3xd8wUA8mefBXpA_image.png)

### **Scenario**

### **Starting point**

### **Instructions**

1\) Lizzie uses her mobile app as every day and sees information about the MyBarista subscription and Coffee Quiz. She ignores the messages for now.

`Open the mobile app, make sure you are logged in. Show the offers from Offer Decisioning proposed to her based on Lizzie's profile.`

*(All instructions in green are actions for the demonstrator to perform)*

![](../../assets/62gmpUym1haishrZv4jdl_image.png)

![](../../assets/GpYq_xmEjyiIOCq5lpOIf_image.png)

3\) Few days later Lizzie is browsing her favourite news site: EXP News and sees a Fréscopa Coffee Quiz ad.Visit the[ ](https://builder.adobedemo.com/run/exp-news/entertainment)page: <https://dsn.adobe.com/web/exp-news/entertainment>

![](../../assets/VVYQMoTBSoebYTObLXAul_image.png)

She clicks on the ad and lands on Fréscopa home page. She is an unknown user on this device.&#x20;

*Click on the ad. It will transfer you to a dedicated page. Right now Lizzie has been assigned to a segment "Interested in Coffee Quiz"*

![](../../assets/2EusvT2MSgG7t_tsF3UeV_image.png)

Lizzie takes the quiz. She is a frequent coffee drinker as she drinks 3-4 coffee cups per day. She also selects Coffee Pods as her favourite way of making coffee.

`Based on her choices she is assigned to a few segments:`

`Frescopa - Frequent Coffee Drinker and Frescopa - Coffee Pods Users. You can open the profile viewer or Lizzie's profile in AEP to show the segments.`

![](../../assets/whS9Kbq4M1XJKKSHZEVYU_image.png)

At the end of the quiz, Lizzie is asked to register to see quiz results. She already has account with Frescopa, so she signs in to the web page. &#x20;

`Sign in to the website with the account created in the Prerequisites.`

![](../../assets/QhIqFrA6rUX_cnpiPPeMi_image.png)

Lizzie can now get familiar with the quiz results and learns about perfect coffee for her: "Morning Muse".&#x20;

`Open the profile viewer and show how the anonymous profile was merged with all we know already about Lizzie, that she is also a Smart Machine Owner. You can also go to the AEP Profile and show all Lizzie's interactions there.`

![](../../assets/R7tlvXs6QHzEqZAzcH_Qg_image.png)

She is interested in the new kind of coffee and clicks on "Add to MyBarista" button and sees the form, all the fields are pre-filled with her details. Lizzie is distracted and doesn't have time to learn more about it and she abandons the form for now.

![](../../assets/Ym923lPmmmlvtKNAothV9_image.png)

\[Optional] Lizzie goes back to the Frescopa home page and she noticed that the main banner now displays information about the new coffee: Morning Muse instead of the Coffee Quiz.

`Behind the scenes Target is displaying right banner for Lizzie based on her segments.`

![](../../assets/hOZvKJRqiOjTeY3tmeFSX_image.png)

Few days later, Lizzie is walking next to the Fréscopa boutique and receives a notification on her mobile app, inviting her to the boutique nearby for a free cup of coffee - the Morning Muse Light Roast.&#x20;

`To simulate the store proximity use the Journey Trigger project. Open following link:`<https://dsn.adobe.com/cx/frescopa-jt>`Search for the Lizzie's profile by email (use your demo persona email). Click the "Trigger Journey" button next to "Frescopa Boutique New York". You should get a notification on your phone. Make a screenshot of it as you will need it in the next steps.`

![](../../assets/rJ6LRJOzbTIlbsLijTT6a_image.png)

![](../../assets/HE-WG65elC9S2oNBisoqu_image.png)

Lizzie walks into Frescopa butique and uses her free coffee offer to get one cup of Morning Muse.

`To show this experience Open the Fréscopa Customer Experience App project: `<https://dsn.adobe.com/cx/frescopa-cx-app>`Select QR code option in the dropdown at the top. A new window will show up that will enable your computer camera. Keep the QR code in front of your camera. Click Confirm on the offer. Experience Event will be registered in AEP.`

![](../../assets/NIxwI92WwN8RQ7cuL5f2r_image.png)

The merchant who was giving Lizzie the free coffee, sees her full profile and recent interactions on the screen after she scans the QR Code. He also sees that the next best offer for her is the subscription to the MyBarista program.&#x20;

`Scroll down on the Customer Experience App and present Lizzie's interactions from the merchant perspective. All Lizzie's purchases should be visible there as well`

![](../../assets/reMyjLBbHpsjgxTP-Pq8x_image.png)

The merchant propose the MyBarista program again to Lizzie and this time she says she wants to start the process. The Merchants does that and immediately Lizzie receives an email in her inbox. Also, sees new offer.

`Click "Next". This will trigger a Journey that will send an email to Lizzie. New offer can be seen.`

![](../../assets/yorP4M8BIgqeu4abIW19l_image.png)

![](../../assets/p4Sn4WQ9kjPz4MpCV7vf7_image.png)

Lizzie's mobile app also is aware of the profile change and is not displaying the MyBarista ad anymore. App shows the updated offer.

![](../../assets/Er8rOMN0FQX2M9OKjddMs_image.png)

:::hint{type="info"}
In case, Lizzie does not subscribe using CX app and is not interested right away, she can go back to website anytime and can subscribe there by clicking on "**Add to My Barista**" button

![](../../assets/aUb0-Vng1ZJnSaTD7ldl2_image.png)

![](../../assets/zX0EnHvEdUpC1-Rknf-MY_image.png)
:::

