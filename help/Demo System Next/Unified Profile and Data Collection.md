---
title: Unified Profile and Data Collection
slug: Py1P-unified-profile-and-data-collection
createdAt: Thu Aug 31 2023 10:43:38 GMT+0000 (Coordinated Universal Time)
updatedAt: Sun Apr 21 2024 13:55:47 GMT+0000 (Coordinated Universal Time)
---

Luma wants to learn more about their customers, their online and offline behaviour. They are adding AEP and Data Collection tag to their website and mobile app to gather information about what the users are looking at on the web page and mobile app, observe the purchase funnel and use this information to deliver more relevant and personalised experience.

PREREQUISITES:

1. Start on a new incognito window or reset profile using profile viewer to generate new ECID on the browser for new user&#x20;
2. Start a new mobile session by using the "Reset Profile" button on the settings tab to start with a fresh ECID&#x20;
3. Prepare second user and ingest the data to the platform to have a profile to demo profile attributes, computed attributes, ML scores and segment membership from batch segmentation&#x20;

Scene 1

Showcase we can personalize for brand new user

-

  1. Open the Luma website as anonymous user: <https://dsn.adobe.com/web/luma3>


-

  ![](../../assets/6L73a3RFiPTu0-c4kNppJ_image.png)



- 2\. Navigate to any category page
-

  ![](../../assets/2IQvHZ0rIIoc1eFJdqvIi_image.png)



  ![](../../assets/YavSE8BSzXAdYEGnSAPZ2_image.png)

* 3\. Browse any product
*

  ![](../../assets/hGbCJJYnqHkwQHEjHViJd_image.png)

- 4\. Open profile viewer. The product view event will be visible in the Experience Event Section
-

  ![](../../assets/e0-2-w6XY3eNPIg014OW0_image.png)

* 5\. Click on the "Sign in" button in the top right corner
*

  ![](../../assets/v0Cz6D8jixsWxRAirwNdT_image.png)

- 6\. You can login if your profile already exists in AEP or register.&#x20;

  For this scenario click "Create an account".

  Fill the required fields and click "Register".&#x20;
-

  ![](../../assets/buhpA8MPCXotuWMfLkvVQ_image.png)

* 7\. Open profile viewer - Profile details should be visible there. You will also get an email with Registration Confirmation - check the "Triggering Journeys - Registration" scenario to learn more.&#x20;
*

  ![](../../assets/7BKUF5XJlbgKttOn7bWFB_image.png)



  ![](../../assets/TxiKtZR6gOmI1yuqByb01_image.png)

- 8\. Open again any product. Add it to the cart.
-

  ![](../../assets/aAsvha2kYDQtI-3nyHQPk_image.png)

* 9\. Click on the cart icon in the top right corner
*

  ![](../../assets/iQRujo_PI4NP8FQ4hJ_ZX_image.png)

- 10\. Proceed with the checkout process
-

  ![](../../assets/4yf0lp6tH-jnUo-MbiLCv_image.png)

* 11\. Review your order. If you won't click the Confirm Order button fast enough you will get an email message (Check the Cart Abandonment scenario). Click "Confirm order"
*

  ![](../../assets/78thuK1Hkr3Y89mBuJT2M_image.png)

- 12\. Open profile viewer. The "add to cart", "purchase" and "checkout" events will be visible there.
-

  ![](../../assets/7KD8g9ANBGJKez5QLKIaf_image.png)

* 13\. Open the mobile app on your phone. Make sure you are connected to public Luma project (Go to settings screen to check).
*

  ![](../../assets/QD2VST2yFrFHxVA0z8vM0_image.png)

- 14\. Browse any product, add it to cart.
-

  ![](../../assets/KCrlekQDzk7UTm5t_lNtg_image.png)

* 15\. The "product view" and "add to cart" events be visible in the Profile Viewer (swipe from left to right to see it). Close Profile Viewer.
*

  ![](../../assets/rvasdxwqUplekxcJdYKkB_image.png)

- 16\. Click the user icon in the top left corner to login. Use the same email address as you used on the web page.
-

* 17\. Both, web and mobile, profiles will be merged. You should see all profile details experience events and segments shared between the devices.
*

  ![](../../assets/_uvdXF9hstnsluitlwgU5_image.png)

- 18\. If there were segments in the web page "Interested in Women's/Men's category" - the app will be updated with personalisation activity.
-

  ![](../../assets/tndMjAyEa3RmXbIBdqXA0_image.png)

* 19\. Refresh the web page - all mobile interactions will be visible there
*



  ![](../../assets/b8LoqA6N33WENQDG98BGi_image.png)

  ![](../../assets/xl8RmwZpau9AdhxOIHDHq_image.png)

