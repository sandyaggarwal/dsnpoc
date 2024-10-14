---
title: Mobile Experience Targeting
slug: 7UbK-mobile-experience-targeting
createdAt: Tue Jun 04 2024 12:50:58 GMT+0000 (Coordinated Universal Time)
updatedAt: Tue Jun 04 2024 13:06:01 GMT+0000 (Coordinated Universal Time)
---

Adobe Target helps test, personalize, and optimize mobile app experiences based on user behavior and mobile context. You can deliver interactions that engage and convert through iterative testing as well as rules-based and AI-powered personalization.

The Adobe Experience Platform Mobile SDK is the recommended solution to power Adobe Experience Cloud solutions and services in your mobile apps.

### Prerequisites

1. A mobile project created connected to your IMS ORG - check the integrations tab to make sure the app will send data to the proper instance. If you dont have a project, create a new mobile project e.g. [https://dsndocs.adobe.com/docs/retail-demo-environment ](https://dsndocs.adobe.com/docs/retail-demo-environment)
2. A mobile property created in Data Collection
3. Edit access to Target
4. Audiences created and shared with Target. [How to use AEP Audiences in Target using Destinations](<../Demo System Next/How to use AEP Audiences in Target using Destinations.md>)
5. DX Demo app installed and connected to your project.

### Steps:

- 1. Go to <https://dsn.adobe.com/> and open your mobile project. Make sure the "Screens" tab is selected.


-

  ![](../../assets/QU-3chDMAkOaSlEI6b228_image.png)

* 2\. Select the screen that you want to use personalize (each screen can be personalized separetly using different mbox name).&#x20;

  For the purpose of this example we will personalie the Home screen. Select it in the UI so that the screen details would be visible on the right.

  Expand Personalization section on the right.


*



  ![](../../assets/LlEQ-XY9TpF153N2hmcrL_image.png)

- 3 Select Adobe Target

  Provide the mbox name, make it unique e.g. your project name + screen name

  Clicking on "Sample offer content" will display a sample you can use in your Personalization Activity. You can change the content manually by updating the fields and json structure.
-

  ![](../../assets/2i_Hk5TsSOY3SJnvGee0b_image.png)



  ![](../../assets/SdX3GNoWO8-WtjM042lq3_image.png)



- Prepare your Experience Targeting Activity in Target.
-

  ![](../../assets/6xDvibIdpjWn6w9fW0t2T_image.png)

* Choose a location (one or more) - depending on how many mboxes you have set up in your mobile project. Your mbox name won't be probably available in the UI at this moment, type the same name manually that you used in step 2.
*

  ![](../../assets/ZRz4fSjZ1xHYe5qzXulQL_image.png)

- 5\. Add more Audiences and appropriate experiences. Create json offers for them with proper content updates.
-

  ![](../../assets/FxTU6eINpErTECGAX3R5F_image.png)

* 6\. Publish the activity to make it live.
*

  ![](../../assets/6jwRZzX3Ddc3yJ0SGVHR9_image.png)

