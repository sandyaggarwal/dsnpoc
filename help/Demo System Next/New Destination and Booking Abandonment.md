---
title: New Destination and Booking Abandonment
slug: Wozb-data-collection-and-new-destination-campaign
createdAt: Fri Aug 25 2023 14:24:17 GMT+0000 (Coordinated Universal Time)
updatedAt: Thu Nov 30 2023 09:15:17 GMT+0000 (Coordinated Universal Time)
---

### **Business Objectives**

WKND Fly wants to learn more about their customers, their online and offline behaviour. They are adding AEP and Data Collection tag to their website and mobile app to gather information about what the users are looking at on the web page and mobile app, observe the purchase funnel and use this information to deliver more relevant and personalised experience.

### **Scenario**

:::hint{type="info"}
To start with a completely empty profile, clear your browser cookies or open a new incognito window. You can also use the "Reset profile" button at the bottom of profile viewer.
:::

-

  1. Visit the WKND Fly home page

  <https://dsn.adobe.com/web/wknd-fly>
- ![](../../assets/xfSy0QqLQjvLIM3FZvM7i_image.png)

* 2\. Click on the Travel Ready guide
* ![](../../assets/tR9Cd6ecTeEn1FPgoxWgD_image.png)

- 3\. Open the Profile Viewer. The page visits will be tracked. Information is being sent to AEP
- ![](../../assets/fDe5DDbrgNve8SnxiSdNN_image.png)

* 4\. Go to "Destinations" page using the top navigation
* ![](../../assets/dSzZPsOP77cfKcdwigz6I_image.png)

***

- 5\. Select Poland. Notice, in profile viewer, that this view was also tracked in the Profile.
- ![](../../assets/ngkyaIiLnP5MIjjX-73H__image.png)

***

- 6\. Open profile viewer. In the Segment section you should see **WKND Fly - Interested in destination: Poland** segment.
- ![](../../assets/v-4Pw2dhYXaYA11fdYH8U_image.png)

***

- 7\. Go back to destinations and select Mexico. Again this event will be captured as Experience Event. Segment: WKND Fly - Interesed in destination Mexico will be resolved
- ![](../../assets/wbwnov2GU9YpkA6Q9Mq-r_image.png)

***

- 8\. Go back to the home page. The banner will be updated with information regarding trip to Tulum. The activity is designed for people interested in a trip to Mexico.
- ![](../../assets/CpGhp9sIKKynEx4jCu8Ll_image.png)

***

- 9\. Search for a flight.&#x20;
- ![](../../assets/47eQc5iuZpduDokG1JPIa_image.png)

***

- 10\. Notice that your search has been tracked as an experience event (flight.search)
- ![](../../assets/bEXbe4WS-3ixhHiVh27Aj_image.png)

***

- 11\. Select one of the flights and proceed to the checkout. Do not book the flight. ("Don't click Confirm Purchase")
- ![](../../assets/yWqZyM0LaOdVSReRFdnbp_image.png)

***

- 12\. Go back to the Home page by e.g. clicking on WKND Fly logo. You should see an offer from offer decisioning encouraing you to finish the booking. This is an offer from offer decisioning. You can also check the Profile Viewer. Segment "WKND Fly - Abandoned Booking" should be resolved against the profile.

  Click "Finish your booking" button.&#x20;
- ![](../../assets/5ZlFqMvGIZMUAj1gYJNVJ_image.png)

***

- 13\. Fill all the required fields.&#x20;

  Make sure your phone number is a real number but end it with "+randomnumbers". e.g. if your real number is +48123456789, you can use number as follows:

  +48123456789+123 or +48123456789+99999 - just make it unique

  Rember also to make your email unique e.g. (yourldap+numbers\@adobetest.com) zkorczyc+001\@adobetest.com&#x20;

  Make a consious decision if you want to sign up for WKND Fly Club - as this will change the offer in the SMS and Email.

  Click I want to get SMS with booking confirmation.

  Click "Confirm Purchase" to finish the booking process.
- ![](../../assets/EWoXBtcJAc5pW3OD7tS8Z_image.png)

  ![](../../assets/gQ-GjASV8t_JVxRqFrSZz_image.png)

***

- 14\. Your actions has been tracked. Also your profile has been updated with new informations.

  Check the segments as well.&#x20;
- ![](../../assets/fWEEILvI4aAKqssAkk17K_image.png)

  ![](../../assets/RYXuI09CGJ0Z8wTEkpPCi_image.png)

***

- 15\. Soon after the booking you will receive an email with booking confirmation
- ![](../../assets/iOGVOOiTE1Ol-JLOf8B3I_image.png)



- 16\. If you selected checkbox to get sms with confirmation, check your phone. You will get an sms with offer based on your WKND Fly Club Membership.
- ![](../../assets/LznJe1ezxOPw7jnsq3NAr_image.png)

  ![](../../assets/7IikeRx8ereTkqTRYpl-7_image.png)

