---
title: Improved Customer Support
slug: fdBR-improved-customer-support
createdAt: Sun Apr 21 2024 15:55:50 GMT+0000 (Coordinated Universal Time)
updatedAt: Wed Jun 05 2024 13:24:52 GMT+0000 (Coordinated Universal Time)
---

### Business Objectives

It is a high priority for Luma to provide a great customer experience. Important role in their strategy playing advisors, who are helping customers with their problems e.g. with purchase process and take care of after sales support. Luma has the branded call center and a dedicated website chat bot, with which their customers can interact to fail a complain, ask for advise or inform about a problem.

### Prerequisites

1. Create an account on luma website
2. Make a purchase of any product
3. Log in in the Luma mobile app project with the same email as used in the web

### Scenario

Starting point: [[https://dsn.adobe.com/l](https://dsn.adobe.com/cx2/luma3-cx-app)uma3](https://dsn.adobe.com/cx/luma3-cx-app)

:::hint{type="info"}
Use a new incognito browser session to start with a fresh ECID and make sure your profile won't be merged with a previously created profile.
:::



- After a successful purchase, Alice receives her product: Juno Jacket. The package was damaged and so was the Jacket. Alice decides to file a complain. She visits Luma website to learn how to do that and starts interacting with Luma chatbot.



  Go to the Luma website and open chatbot by clicking the icon in the bottom right corner.

  *(All instructions in green are actions for the demonstrator to perform)*
-

  ![](../../assets/9A1MZmGj62-vmg4wk4kI5_image.png)

* Select "I have a complaint" from the list of chatbot options
*

  ![](../../assets/eSdpLOK8tm_fwBELU3vz4_image.png)

- Alice is selecting the answer: Problem with the shipment



  Select "Problem with the shipment" in chatbot window
-

* Describe the situation and finish the conversation with bot
*

- Alice's complain from chatbot is assigned to Melanie - Luma Customer Advisor. Melanie searches for Alice's profile in the Call Center app to learn more about her case and her previous experience with Luma.&#x20;

  Go to the Luma Call Center UI: 
-

  ![](../../assets/c8Tn5tWVOe-R1lalzq4y5_image.png)

* Using the call center UI Melanie, can evaluate Alice's profile. Considering her purchase history and scores it is required to take care of Alice's good customer satisfaction.
*

  ![](../../assets/tNGo2w8htr6-UB6V5w_i9_image.png)

- Melanie calls Alice on her phone and talks with her about her complain.&#x20;



  Find the contact module and click "Phone Call".

  Click "Start the call"

  Select Call Topic: Complaint, add sentiment and comments if needed. Click "Submit" - all these details will be available in the user profile in AEP and on the activity timeline

  End the call
-

  ![](../../assets/jaRio8fdsbDXKgq0LqJ7M_image.png)



  ![](../../assets/MMMUuixyjfvIUeILlM3Vn_image.png)

* During the call, Melanie propose Alice that she can replace the Jacket in the closest Luma KIOS. She sends a push notification with a QR code to pick up the item.&#x20;



  Trigger the push notification using the Event Trigger Module located in the Call Center UI (Send KIOSK replace code to customer)
*

  ![](../../assets/Cx7GdI3GHlHRbm7B_3Rc__image.png)

- Alice receives the link to QR code in a push message.&#x20;



  Long press on the push message to see the qr code.&#x20;
-

  ![](../../assets/Q2S0fDflW4M3Kx_Urp_69_image.png)

* Melanie also asks Alice if she wants to answer few questions about her general experience.&#x20;



  Using the survey module, you can choose the appropriate response, ranging from strongly disagree to strongly agree. Submit buttons trigger a customer satisfaction score update.
*



  ![](../../assets/DieLdRpJZwWTmamOO931z_image.png)

- Next day Alice goes to Luma KIOS and scans the QR Code to pick up the replacement for her Juno Jacket.




-

  ![](../../assets/8Njt8nqVqbRdjjeGs-evf_image.png)



All interactions with Call Center are stored in Alice's profile. You can also refresh Activity view to see the events there.











