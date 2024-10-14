---
title: Back In Stock
slug: Y47K-back-in-stock
createdAt: Tue Mar 05 2024 06:45:06 GMT+0000 (Coordinated Universal Time)
updatedAt: Tue Mar 19 2024 15:47:36 GMT+0000 (Coordinated Universal Time)
---

### ****[**Click here to access the Journey**](https://experience.adobe.com/#/@demosystem4/sname\:public-luma/journey-optimizer/journeys/journey/b0caedd9-473a-4a6d-be83-d59b7560ef16)

## **Goal**

Consumer communication to inform consumers the product they have added to their wishlist is back in stock

## **TARGET AUDIENCE**

Users who engaged in online shopping by adding items to their wishlist through the Luma website but the product was not available in the stock

## **JOURNEY STORY**

Sarah browses the products on the [Luma Retail Website](https://dsn.adobe.com/web/luma3/product?productId=WJ06) and looks at the "Juno Jacket" in women's category products. She likes it and adds it to her wish list by clicking the add to wishlist button

![](../../assets/z5IBrenz4C_DIlOvLT0tq_screenshot-2024-03-05-at-122637-pm.png)

Check the products added to the wishlist in the profile in AEP -> profiles

![](../../assets/vN-5av_vCEC6fzrjCT6H9_screenshot-2024-03-05-at-124506-pm.png)

Inside the journey, the newly added wishlist product will be validated against the wishlistArr. If there is a match with an existing item, the below email will be triggered.

![](../../assets/OdNa6dm_HfdL-ClP-pt6-_screenshot-2024-03-06-at-31359-pm.png)

### **BEHIND THE SCENES:**

**Business Event Schema **we are using is [Demo System - Product Schema for AJO Business Event](https://experience.adobe.com/#/@demosystem4/sname\:public-luma/platform/schema/browse/https%3A%2F%2Fns.adobe.com%2Fdemosystem4%2Fschemas%2F8a4c4e09bb8983e5a6a22102204925f2a5b40042be57220)

**wishListSkuArr** object for storing the items the user has added to the wishlist is stored under path **\_demosystem4.individualCharacteristics.wishListSkuArr in** [Demo System - Profile Schema for Website (Global v1.1)]()

****[Luma - Recently Saved For Later]() Audience is used in the journey under **Read Audience**

**Journey**:

- Business Event - Luma Stock Replenishment
- Read Audience - Wishlist Product without purchase (Save for later)
- Condition: Check if the product selected in the wishlist is the back-in-stock product in the business event
- Condition: Check marketing consent
- Messages (Cross channel):
  - Email: Replenishment Message
  - Push
  - In-app
- End

**LAUNCH: **

Launch rule is updating the wishlist items in the profile.
