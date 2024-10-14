---
title: Drive customer engagement using AJO
slug: oawH-drive-customer-engagement-using-ajo
createdAt: Tue Jun 25 2024 10:30:07 GMT+0000 (Coordinated Universal Time)
updatedAt: Thu Jul 11 2024 08:22:41 GMT+0000 (Coordinated Universal Time)
---

Carvelo wants to keep the 90 customers happy with their service and lower the possibility of them leaving the brand on the lease end. A multiple campaigns were created to keep the customer satisfaction on the high level and prepare them to easy transition to the next lease.

### PREREQUISITES

- Create the demo profile by visiting the Carvelo registration page: <https://dsn.adobe.com/web/carvelo2/create-account>

  For the phone number provide your real number with suffix to recieve sms messages. eg  +48608xxxxxx+1234 (area code, number, +sufix)

  Make sure you gave all consents to recieve emails and sms's.

  You should receive an email once profile is created.
-

  ![](../../assets/vmv0RwTTH8pmnwR32opQm_image.png)



  ![](../../assets/01eTI_zWE8vl6x9QSKePf_image.png)

* Use different browser, or incognito window or reset the profile to start as an anonymous user. You can use the "Reset Profile" button in Profile Viewer panel.
*

  ![](../../assets/pH1dqJj8O0KVWVP1Pv1Bh_image.png)

- Log in to the mobile app: Open the DX Demo mobile app. Select Carvelo from the public projects list on the app Settings screen.

  Click the user icon in the top left and provide the same email as used in the registration above, on the login screen.&#x20;

  :::hint{type="info"}
  You might need to wait few minutes for the email identity being accessible in Platform, allowing you to log in.
  :::


-

  ![](../../assets/iEUDGgGLKg8_SsEHxvQmS_image.png)



  ![](../../assets/1dA1X41UXxRLeprmDMTHp_image.png)

### DEMO PERSONA


Sarah, 35, married with two kids, drives a 2019 Model A. She is happy with her car but her lease is set to expire in 90 days. &#x20;

### SCENARIO 1

- Sarah is browsing a news web page, politics section and sees an ad of the new Carvelo Electric Models. She’s intrigued to see what’s new as she likes her current car but it’s ageing and it struggles to fit the camping equipment.&#x20;

  Open the website: 
-

  ![](../../assets/ajz7XpCdDrRworomyAP7T_image.png)

* She clicks on the ad and reads about the latest Carvelo electric models and is intrigued by the new E-V Model. She goes to the Electric EV Model page.&#x20;

  Click on the E-V Model card

  As this is her new laptop, Sarah stays an anonymous user for now. However, after browsing the website, Sarah is assigned to an Audience: Carvelo - Interested in E-V Model.&#x20;


*

  ![](../../assets/FaBa-afuHMDZIfas47t3C_image.png)



- Few days later she receives an email to her inbox from Carvelo letting her know her lease is coming to an end and that they have some exciting new deals. That's aligned to Carvelo strategy, which sends emails 90 days before the lease is about to expire with private offer based on customer payments and inform about next lease proposal.

  To simulate this event we will use the event trigger project in DSN. Go to this link: **

  **Click "Trigger event" button next to "Lease Close to an end event". This action will trigger a journey. 




-

  ![](../../assets/kyDYOtLOro_THPpr-Tgid_image.png)



  ![](../../assets/XdwA5F-geOo3nVRuNJpNm_image.png)

* She clicks on the offer about bulding your own model and is led to a Carvelo page.&#x20;

  We can now back date the anonymous data to her current profile and update the banner creative to reflect the new profile information through Adobe Target. We can see that she is known to us and has signed in for marketing communications. &#x20;

  Click on the email button linking to "Build your own vehicle" page. The segment interested in E-V should be there and her ECID from anonymous session should be merged with her email address from link she clicked in the email. It might take some time for the profiles to merge
*

  ![](../../assets/9nwu4S5S8MbjT_nqgo_Ws_image.png)



-
-

* She starts building her car but as she’s getting towards the end when the travel agency rings to say she needs to pay for the flights or the last few seats will be sold, so she stops what she’s doing to book the trip.  She abandones the car configuration.&#x20;

  Start interacting with the car configurator but don't submit "Request the quote" form.


*

  ![](../../assets/XFQlsWPnVAJqA_2eMtdOB_image.png)





- The next day she gets an email reminding her that she was part way through configuring her car, she’s intrigued that they’ve finished the last few parts, and at such a good price she clicks through to see what car she could be hers

  Behind the scenes:

  An AJO is triggered to send her an email with her configuration details and calcuated price. It also sends a link to book a test drive.

  An email should reach your inbox, Click on the "Book your Test Drive now"


-

  ![](../../assets/vjLVXPotnGmBdwv1FAnzA_image.png)

* As Sarah is happy with the current experience, she fills all the required fields and schedules a test drive.  After some time she receives an email with all the details.

  Click the "Schedule test drive" button.


*



  ![](../../assets/SAYNTjSlgfV0OgBPEzC8t_image.png)

  ![](../../assets/gnk1zz1v5dPu1l8JkaAH5_image.png)

- The day of Sarah's test drive has arrived and in the morning she recieves a push notification with a reminder, hour and place of the meeting.&#x20;

  If you are signed in in a mobile app, you will recieve a push message. In the other case you will receive an email message.

  You will also recieve an SMS message if your number is valid.


-

  ![](../../assets/cN6R1XEY3Ts3zJ9I1Uan1_image.png)

  ![](../../assets/PMp5wIeoQyTzY6uR9qp9c_image.png)

* On the day of her test drive, Sarah walks onto the lot. A sales agent welcomes her and leads to a sales rep who will help her with the test drive. When she completes the test drive she receives an email providing her a link to check a special car loan.

  To simulate the test drive attendance, use DSN event trigger project: Open the email that will arrive to your inbox and click on the "Car Loan" link.


*

  ![](../../assets/zbe7gHutTNiQZOuVSlkok_image.png)

  ![](../../assets/zOYnqW9lEcSteP_lYifwJ_image.png)

- She fills in her personal and financial details to apply for a loan, ensuring all the required information is accurate and complete to expedite the approval process.

  Fill all the required fields in the form. Click "Submit" on the last step.
-

  ![](../../assets/kfh2J9vLxD7fCsxP-8CiN_image.png)



  ![](../../assets/3YBmpQuAelnGyc579ugeG_image.png)

* Sarah receives an email notifying her that her preapproval letter has been accepted.
*

  ![](../../assets/lAMbBurketOl1M5Dnpem5_image.png)

- A few days later, she receives an email requesting her to review and sign the loan documents. This step is crucial for finalizing the loan approval and securing the funds she needs.


-

  ![](../../assets/tzsYemQ51P4bpk4M3GM_7_image.png)

* She clicks on the link to sign the document.
*

  ![](../../assets/Llt6g9JQ10MXgrl-S--DM_image.png)



  ![](../../assets/ncUHJuTTwYpvmBQ64eWNd_image.png)



  ![](../../assets/B99wQVI_hIOL9FyfvsXNf_image.png)

- After signing the loan document, she receives an email asking her to confirm her email address. She clicks on the link to complete the confirmation.
-

  ![](../../assets/ZPcWs4rYp5LvXF947zDPr_image.png)



  ![](../../assets/ldQxgBv8PvP2crmnHdKq__image.png)



###

###



