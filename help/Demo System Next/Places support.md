---
title: Places support
slug: -i61-p
createdAt: Tue Jun 04 2024 08:14:10 GMT+0000 (Coordinated Universal Time)
updatedAt: Thu Jun 20 2024 20:56:05 GMT+0000 (Coordinated Universal Time)
---

Places Service, previously known as Adobe Experience Platform Location Service, is a geo-location service that enables mobile apps with location awareness to understand the location context by using rich and easy-to-use SDK interfaces accompanied by a flexible database of points of interests (POIs).

Places Service allows us to :

- Create and manage a database of POIs that can be leveraged with other Adobe Experience Cloud solutions.
- Configure the SDK in Adobe Experience Platform Launch to define location-triggered rules and metadata based conditions.
- Reduce the code that we need to write to monitor a device’s location and use the Places extension to automatically trigger the location-specific rules.

### **Manage libraries**

1.Go to Data Collection. Click on Places under Data Management.  &#x20;



![](../../assets/arh6jVSV_iFVU35ugiKT1_image.png)

2.On the top right side, click … > Manage Libraries.



![](../../assets/Ytr2U5xqKzcskTZuRIumC_image.png)

3.Click **New**. Provide a name and click **Confirm**.



![](../../assets/7bFl-4op3BWdM-2mKjWvk_image.png)

### **Create a POI**

1.In the top right side, click New.



![](../../assets/2dbp7Yo2jja-2NCRmoYwF_image.png)

2.Provide a name for the POI. Enter or select a radius.



![](../../assets/xW2C0nJ7yFfr960T7NPjP_image.png)

3.The following steps are optional:

1. Select an icon for your POI.
2. Select a color for the icon.
3. Specify a category for your POI.

4.Expand the **Location** section.

1. Type an address.
2. Type the city.
3. Type the name of the state.
4. Type the name of the country.
5. Select or enter a latitude or longitude (required).
6. Click

If you do not know the exact latitude and longitude, dropping a pin is useful.



![](../../assets/tXBIUGO5ENLswJdG_unIO_image.png)

### **Install Places extension**

1. Go to Data Collection and open the property.
2. Click on **Extensions** tab.
3. On the Catalog tab, locate the Places extension, and click Install.



![](../../assets/yFZBw1_0PvJtcLeKjizMQ_image.png)

4.Select the Places libraries you want to use in this property. These are the libraries that will be accessible in your app. Click Save.



![](../../assets/JPXKPVooIyzxrkxOTCauz_image.png)

### **Create a rule:**

With the Places extension and a region monitoring solution installed in your mobile application, you can create rules in Adobe Experience Platform Launch that are triggered or conditioned location data including location entry and exit events.

1.Create new Rule called e.g. "Enter POI"&#x20;



![](../../assets/pvGB9pBcMsXdTIllbl6x__image.png)

2.Add an event as below:

Extension: Places

Event Type: Enter POI

Name: Places - Enter POI





![](../../assets/1JxzohyrjyOF_rAppYxTC_image.png)

3.Add an action as below:

Extension: Mobile Core

Action Type: Send Postback

Name: Mobile Core - Send Postback

&#x20;Url: Provide web hook url to which message should be sent.

Post Body:&#x20;

> { "text": "DSN entered POI region {%~state.com.adobe.module.places/lastenteredpoi.regionname%}." }



![](../../assets/Uq4p3xBfVRNFbaJ9i13Ed_image.png)

This is a basic rule for tesing poi entry by sending slack notifications.&#x20;

**Note**: Advanced usecase -You can  also  add "Attach Data" to send location.entry event to trigger push notifications.

> {
>     "xdm": {
>         "eventType": "location.entry",
>         "_demosystem4": {
>             "identification": {
>                 "core": {
>                     "ecid": "{%%ECID}"
>                 }
>             }
>         }
>     }
> }



![](../../assets/OY1RXv0bZs8tjPQRZaPWw_image.png)



![](../../assets/mS859xw0Llz0MmFb4csHG_image.png)

4.Complete the publishing process to update the SDK configuration.

### **Use Adobe Experience Platform Assurance for Places Service**

1.Go to Data Collection and click on Assurance.



![](../../assets/FX_zgMAPhCZ5EoTvErWEr_image.png)

2.Connect app to assurance session. To learn more : <https://dsn.adobe.com/docs/use-assurance>

3.From the left side menu, select the Map & Simulate.

![](../../assets/MAgo49aMyZN0euJaZUxoX_image.png)

4.On the map find your desired area and click "Simulate Load POIs"

![](../../assets/Rkptw63KgqgBvKu4JOFjz_image.png)

5.Click on the pin that will show up and click "Simulate Entry Event".



![](../../assets/O67Tx_-TOaI6zjuKPMFOn_image.png)

6.The mobile app will receive this event and a notification will be sent to the slack channel.

Demo Scenario to show Places support in DSN public projects:

- Luma [In-app support](<../Demo System Next/In-app support.md#kAUor>) demo description

