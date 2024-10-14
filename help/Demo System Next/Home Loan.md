---
title: Home Loan
slug: f3ok-home-loan
createdAt: Wed Oct 25 2023 19:30:31 GMT+0000 (Coordinated Universal Time)
updatedAt: Fri Oct 27 2023 13:09:10 GMT+0000 (Coordinated Universal Time)
---

### Background

This scenario follows Haley Smith through the experience of applying for a home loan. She's already a SecurFinancial customer and is looking for a house on external real estate website. SecurFinancial has a partnership with that website which enables more personalized experiences for SecurFinancial customers.

Refer to the [Retail Banking Industry Journey](https://internal.adobedemo.com/content/demo-hub/en/demos/internal/fsi-retail-banking-xd.html) for the full story.

### Before you begin

- Make sure you have the [DX Demo Mobile app](https://dsn.adobe.com/install)
- Switch mobile app to the SecurFinancial public project.
- For this scenario you will need a profile that already exists in AEP, sign in with that profile in both website and mobile app.&#x20;

### Steps

Starting point

Home page with additional parameter to simulate searching for a house: <https://dsn.adobe.com/web/securfinancial2?keywords=house>

- Haley is looking for a house on House Find website. This action puts her in "Looking for a house" segment and SecurFinancial uses this information to personalize the home page for her making the Home Loan page accessible with one click.

  `Click "Learn more" on the banner.`
- ![](../../assets/KlX4MktqJ8EkmHk1EQiVT_image.png)

* Haley navigates to the  SecurFinancial Home Loan page which contains a mortgage calculator. Here, Haley can easily calculate the monthly payment  and decides to apply.

  `Click "Apply now".`
* ![](../../assets/Ihv5xhsYYszIX5pmrelPb_image.png)

- Form is already pre-populated with Haley's data which simplifies the process. She fills out the form uploading necessary documents and submits her application.&#x20;

  `Complete the wizard and click "Submit" at the end.`
- ![](../../assets/Ay2URn1uhWhHfKsKP0spD_image.png)

* Haley receives a confirmation email.

  `Wait a moment for the "Preapproval letter accepted" email. `
* ![](../../assets/l3ON0zS7BknavCwuh9mud_image.png)

- Haley likes the property she found so much that she decides to make an offer. Using the SecurFinancial mobile app, Haley sends her preapproval document to the realtor.

  `Switch to the mobile app. Make sure that you're logged in using the same email that was used on the website. After logging in, go to the "My Documents" screen and click "Send to realtor".`
- ![](../../assets/0ipsnc6gHkTViix7h2mAI_image.png)

* After sending the document, she receives a confirmation email.

  `Wait a moment for the "Information for when the house goes under contract" email.`
* ![](../../assets/m3MYbPAS8pZ-rJ-EC3_9r_image.png)

- Some time later, Haley receives another message confirming that her closing documents were accepted.

  `Another email ("Closing documents accepted") is sent ~10 seconds after the previous one.`
- ![](../../assets/DIPJaudSK62ALm8cNVlXs_image.png)

### Journeys

Following journeys are started during this scenario:

1. [SecurFinancial - Home Loan Offer](https://experience.adobe.com/#/@demosystem4/sname\:public-securfinancial/journey-optimizer/journeys/journey/5a13643a-9a58-49fd-906b-c3befbcd1b3a)
2. [SecurFinancial - Home Loan Application](https://experience.adobe.com/#/@demosystem4/sname\:public-securfinancial/journey-optimizer/journeys/journey/f92af885-d68c-47a2-9015-3bc4f20497e6)

