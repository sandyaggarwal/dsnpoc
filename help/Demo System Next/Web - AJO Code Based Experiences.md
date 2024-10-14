---
title: Web - AJO Code Based Experiences
slug: psPA-code-based-experiences
createdAt: Wed Apr 10 2024 05:29:59 GMT+0000 (Coordinated Universal Time)
updatedAt: Wed Jun 19 2024 06:43:26 GMT+0000 (Coordinated Universal Time)
---

This section details how to configure AJO Code-based experience in a DSN Web project such as Luma created using the Quick Setup.

### **Prerequisites**

In order to showcase the capabilities of the AJO Code-Based Experience, you must ensure that you have met the following prerequisites:

- - A DSN Web project connected to an AEP Launch tag property


-

  ![](../../assets/ETQD3EkjvRFWv8zrirkBH_cleanshot-2024-05-03-at-153906.png)

* * Your data stream should have the Journey Optimizer checkbox checked
*

  ![](../../assets/qfkxIJmzSnLHz6kzFzstS_cleanshot-2024-05-03-at-152221.png)

### &#xA;**Step-by-step configuration**

### Create a new AJO Code-Based Experience Campaign

1. Go to **AJO Campaign**
2. Click on **Create Campaign**
3. Select Action as a **Code-based experienc**e, set the surface to set the surface to <web://dsn.adobe.com/web/abcd-1234/>
4. Enter a Campaign name such as **Luma - Exclusive offer**
5. Set the audience to **All visitors (default)**
6. Set the Identity type to **ECID**
7. Make sure to replace the project id **abcd-1234 **with your web project ID in the following content then copy and paste it into the campaign JSON content:

```javascript
{%#if profile.person.gender = "male"%}
{
  "title": "{{profile.person.name.firstName}}, get a unique discount on our new Luma Gear collection",
  "description": "REACH NEW HEIGHTS WITH ULTIMATE LUMA GEAR",
  "link": "https://dsn.adobe.com/web/abcd-1234/men-products",
  "imageUrl": "https://demo-system-next.s3.amazonaws.com/assets/luma/AdobeStock_258726216.jpeg",
  "code": "MEN20"
}
{%else if profile.person.gender = "female"%}
{
  "title": "{{profile.person.name.firstName}}, get an exclusive offer on our apparel collection",
  "description": "UNLOCK YOUR NEXT LEVEL WITH LUMAFLEX™ APPAREL",
  "link": "https://dsn.adobe.com/web/abcd-1234/women-products",
  "imageUrl": "https://demo-system-next.s3.amazonaws.com/assets/luma/AdobeStock_258726216.jpeg",
  "code": "WOMEN20"
}
{%else%}
{
  "title": "Discover the new Luma 2024 Apparel Collection",
  "description": "UNLEASH YOUR STYLE WITH NEW APPAREL COLLECTION",
  "link": "https://dsn.adobe.com/web/abcd-1234/men-products",
  "imageUrl": "https://demo-system-next.s3.amazonaws.com/assets/luma/banners/AdobeStock_570499457.jpg",
  "code": "DEFAULT"
}
{%/if%}
```

8\. **Activate** your Code-based Experience campaign

###

### Update the AEP Launch tag property configuration

To display the experience on the DSN Luma web project, you will have to update the configuration of the Experience Platform Launch datastream and a rule in the tag property.

***Update the datastream configuration***

1. Navigate to <https://experience.adobe.com/>
2. Go to **Adobe Experience Platform Data Collection **using the Solution switch (top right)
3. Using the left menu, click on **Datastreams**
4. Search your datastream by using your LDAP as a filter then edit the datastream
5. Edit the Adobe Experience Platform Service to enable **Adobe Journey Optimizer**



![](../../assets/DbnYc77-3j3GeFM6sT8GJ_cleanshot-2024-05-03-at-152650.png)

6\. Save the changes

The data stream is now configured to get AJO Code-based Experiences. ✅




***Update the Tag properly Web view rule***

1. Using the left menu, navigate to navigate to **Tags **in Adobe Experience Platform Data Collection
2. Search for your tag property using your **LDAP **as a filter then click on the tag property
3. At the top right, select **Main **as the working library
4. Using the menu, click on **Rules**
5. Click on the rule **Page View **to edit the configuration
6. In the **Actions**, click on the **+ **button to add a new action
7. In the action, set the Extension to **Core, **the Action Type to**Custom Code**, set the name to **Code-Based Experience personalization**, set the language to **JavaScript **then click on **Open Editor**
8. Copy and paste the following code in the Launch code editor, make sure to** update the surface URI in the code below with the one you configured in the AJO Code-based experience campaign by replacing the project ID "abcd-1234":**

```javascript
function sendDisplayEvent(decision) {
  const { id, scope, scopeDetails = {} } = decision;
  alloy("sendEvent", {
    xdm: {
      eventType: "decisioning.propositionDisplay",
      _experience: {
        decisioning: {
          propositions: [
            {
              id: id,
              scope: scope,
              scopeDetails: scopeDetails,
            },
          ],
        },
      },
    },
  });
}
 
function applyPersonalization(surfaceName) {
  return function (result) {
    const { propositions = [], decisions = [] } = result;
    // send display event for the surface
    decisions.forEach((decision) => sendDisplayEvent(decision));
 
    const proposition = propositions.filter((p) =>
      p.scope.endsWith(surfaceName)
    )[0];
 
    if (proposition) {
      console.log(" > Offer proposition received: ");
      const {
        title = offerTitle,
        description = offerDesc,
        imageUrl = offerImageURL,
        link = offerLink,
        code = offerCode
      } = proposition.items[0].data.content;
      document.querySelector('.Title__content > strong').innerText = title;
      document.querySelector('.Banner > div > img').setAttribute('src', imageUrl);
      document.querySelector('.Title__content > h1').innerText = description;
    } else {
      console.log(" > No offer proposition");
    }
  };
}
 
alloy("sendEvent", {
  renderDecisions: true,
  personalization: {
      surfaces: ["web://dsn.adobe.com/web/abcd-1234/home"],
  },
}).then(applyPersonalization("web://dsn.adobe.com/web/abcd-1234/home"));
```

9\. Save your changes

10\. At the top right, click on **Build** to update the Launch tag library.

The Experience Platform Data Collection is now configured 🎉. Time to test it!&#x20;



### Test your AJO Code-Based Experience campaign

You can now test the configuration by following these steps:

1. Navigate to your DSN Luma project e.g. <https://dsn.adobe.com/web/abcd-1234/home>
2. Create a new test Profile or Sign in with an existing profile having a gender value set in the Real-time Customer
3. Navigate back to the Home page to display the updated experience powered by AJO Code-based experiences

![](../../assets/QRTO6mOifZoOuB_haRxkT_cleanshot-2024-05-03-at-155519.png)

You have successfully configured a working setup that can be customized as per your demonstration requirements.



Live demo of Web AJO Code Based Experiences:

- **SecurFinancial ATM Screen**: [<https://dsn.adobe.com/docs/atm-screen-code-based-experience>](https://dsndocs.adobe.com/docs/atm-screen-code-based-experience)
- &#x20; **Binji SSR TV app**: [<https://dsn.adobe.com/docs/binji-tv-ssr-app-code-base-experience>](https://dsndocs.adobe.com/docs/binji-tv-ssr-app-code-base-experience)



