---
title: Receive Push Notification from Campaign
slug: TRrj-receive-push-notification-from
createdAt: Thu Mar 28 2024 15:54:01 GMT+0000 (Coordinated Universal Time)
updatedAt: Thu Mar 28 2024 16:15:18 GMT+0000 (Coordinated Universal Time)
---

## GOAL:

Send push notifications on **DX Demo v2.x **from Adobe Campaign.

## Instructions:

**1) Create a Mobile Application in ACC**

Create iOS Mobile App

*Log in to the Campaign instance*

Go to the *Profiles and Targets > Services and Subscriptions *node under Explorer and click **New**

![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2F7VgGcL6sjcvHDlsxFID1%2FScreenshot%202023-06-28%20at%201.52.12%20PM.png?alt=media\&token=1029891b-65e1-417a-95ed-088515c47a3a)

![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2F9edC2Y6Q4JKUc9RYyAlg%2Fimage.png?alt=media\&token=6218abe1-e6f7-4d38-a35f-3fc484b025d5)

2.Define a **Label** and an** Internal name**. Select **Type** field as **Mobile application**.

![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2FsvEe5BoDjpMPKyTDbWO9%2FScreenshot%202023-06-28%20at%201.55.53%20PM.png?alt=media\&token=07f31211-3123-4210-aa05-20f026d8f3ef)

Then click the **Add** button to define the various versions of your mobile application.

![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2Fouka2MVm7W1dmMIkCC2R%2FScreenshot%202023-06-28%20at%201.57.53%20PM.png?alt=media\&token=514e27d3-f65c-438e-be97-2dc51d0bb79e)

![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2FiqUutPiZUYIVc6bcGhEL%2Fimage.png?alt=media\&token=c1020fe4-ec01-4d38-b8b5-5a065c0daf4d)

Click next and create an **iOS application. **Start by entering the **Label.**

Add application variables:

1. mediaUrl
2. mediaExt

![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2F7LyehcKq4wa9qR6jhkVs%2FScreenshot%202023-06-28%20at%202.06.19%20PM.png?alt=media\&token=92c6952a-641b-4a2f-a0d4-c5f68e1bb9bc)

Click Next -> Click the **Enter the certificate iOS (GET iOS CERTIFICATE FROM **[ACC certificate(DX Demo App 2.0)](https://wiki.corp.adobe.com/display/demosystem/Certificates+for+DX+Demo+App+v.2.x.x) **LINK**), then select the authentication certificate and enter the password for the certificate.

`IMPORTANT`**: **This certificate works with Campaign V7, for Campaign V8, you would need Token based authentication and its details are also available here [ACC certificate(DX Demo App 2.0)](https://wiki.corp.adobe.com/display/demosystem/Certificates+for+DX+Demo+App+v.2.x.x)

**NOTE: **You are configuring the development and production application with the same iOS certificate or token-based authentication.

![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2FtfV4EP653CdTUn3ZZ0ol%2Fimage.png?alt=media\&token=5db25943-a510-46ee-baa6-ded73408b022)

Click Next to configure the production application and note the `INTEGRATION KEY`

&#x20;on the notepad since you would need to add this in the launch property**. **

Upload the certificate, test the connection, and click finish.

**This integration key, specific to each application, lets you link the mobile application to Adobe Campaign Classic.**

![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2F9iPloc2VdKJ1yv5lLJMy%2FScreenshot%202023-06-28%20at%202.16.59%20PM.png?alt=media\&token=ff755cb0-6a35-42f4-9ee3-14049e135211)

### Create Android Application

If you are an Android user, create a subscriber application for Android.

Provide **project key**:

`AAAAaqOt1nM:APA91bGD2vfQFDun3t7dCQcbOobPY8Rad0Elh3dyIpYspIx4otRPbi0eMahVQUJf4CF2U1osTyp6D2HvwlcvMRQtVzUcxF6zZ43j8LAzl_GK8birmzUcfDMM0fuQDPPgZ--16MrBwqA6`



## Create mobile application using Demo System Next

1\) Go to <https://dsn.adobe.com/quick-setup>, select the environment and under "`Solutions`" -> select "`Mobile - Push Notifications`" and start the configuration

![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2FnjafHZNrhC8EIdBSTwxk%2FScreenshot%202023-06-28%20at%204.24.38%20PM.png?alt=media\&token=76c126f8-c330-43d7-b26e-a8d3458637ef)

2\) Once the configuration is successful, open the project and the launch property

![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2Fzh1Iqu8gpmyosNb7N7Cf%2FScreenshot%202023-06-28%20at%204.27.27%20PM.png?alt=media\&token=e6fdff2e-5389-431f-9ce7-38249fe0d598)

3\) Attach the launch property to the project by navigating to the "Integrations" tab and clicking the "Edit" button.

![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2FOyVrd0IwYEKDOHFXnOf9%2FScreenshot%202023-06-28%20at%204.29.20%20PM.png?alt=media\&token=06500ffc-9503-4686-b82d-f69507daa500)

4\)  Open the Launch property by clicking view and configure campaign classic in the launch extensions.

![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2Fak3gtnWTBoQB3g7uUfBY%2FScreenshot%202023-06-28%20at%204.37.26%20PM.png?alt=media\&token=ff673e31-d48f-4d09-bf9b-355c934329ba)

5\) Open **Extensions **tab in the launch property. Click "Catalog" -> click "Catalog" -> search "Campaign" and click "Install" on Adobe Campaign Classic

![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2Fd0IiPWVoPeeM6QUhy0hO%2FScreenshot%202023-06-28%20at%204.42.17%20PM.png?alt=media\&token=0954290c-0d9f-40a4-ba5d-a1cf91eaa3bb)

6\) Add the campaign classic instance URL and integration key that you saved earlier.

:::hint{type="info"}
Campaign Classic registration or tracking endpoint URLs can be retrieved under the **Tools > Advanced > Deployment** wizard menu in the Campaign Classic interface. The endpoint for push notifications is usually the same as the URL used for web forms and surveys.

For this extension, the registration endpoint URLs/tracking endpoint URLs should be entered **without **a prefixing https\://.
:::

![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2F6AMX9wTmi5HiBW3difT8%2Fimage%20\(10\).png?alt=media\&token=539988d1-859b-430b-8698-d4f1de5d4997)

7\) Click "Publishing Flow" and build the library.

![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2FrnYIUZ5RyVJU9ANSjMvG%2FScreenshot%202023-07-03%20at%2010.57.36%20AM.png?alt=media\&token=06cb781d-911c-44ef-844d-a83f58071e25)

8\) Go to your project and click run and scan the code in the DX Demo mobile app.

:::hint{type="info"}
Install the latest app on your phone by scanning the QR code available here:

<https://dsn.adobe.com/install>
:::

![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2FexVqYzPnq0p0oALWZI0A%2FScreenshot%202023-07-03%20at%2011.19.10%20AM.png?alt=media\&token=b645019d-1e69-42b4-8a0a-55d332b2fe24)

![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2F9OKVg9M27eMJ64DIaSej%2FScreenshot%202023-07-03%20at%2011.19.04%20AM.png?alt=media\&token=40c9e530-7351-4145-a7be-e75e4dec6fb0)

9\) Open the DX Demo app, go to the Settings screen, click "Custom Project" and scan the project code.



![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2F0Nb2Ci2eVSRXC9zjlP3G%2FIMG_0865.png?alt=media\&token=32c70562-49c6-488a-8155-33c926de40f5)

10\) Make sure you see the device token in the app created in ACC.

![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2FTxMs9etaqky2CD1kYmj1%2Fimage.png?alt=media\&token=23991247-b77e-47c0-b272-fc28e8a7d9d0)

Click on user icon on left in app on device. It will take you to login screen. Click on Create Account.Once you register you will also see the email in ACC next to Registration token.&#x20;

![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2FRwv2HFkdZYyy8nwRRZ1u%2Fimage.png?alt=media\&token=535f37da-4d2d-4bf2-af25-357f9cf8f71a)

:::hint{type="info"}
ACC instance need not be in the same org as AEP.
:::



### Create push notifications

1\) Create a new push notification using the default push template

2\) Click on the "To" to configure the Target

3\) Select **Subscribers of an iOS mobile application (iPhone, iPad)**, select the service relevant to your mobile application, then select the iOS version of the application.

![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2FOTZxBV3i9gN9rnIFovGk%2Fimage.png?alt=media\&token=801fac1d-7bc6-42ed-9a10-63be8dc487c2)

![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2FDpQti94Pdlq3b2cshOcv%2Fimage.png?alt=media\&token=fc2e8c07-0929-4f6b-83c2-d7b8b307c9f9)

4\) Edit the title, message, and mediaUrl then click on save.

![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2FqXIjMUUe4emwir6EYdkq%2Fimage.png?alt=media\&token=51640bbd-dfc9-4a8b-ad18-a36b8c2123db)

You can now send your message using the Send button of the delivery.





![](../../assets/IBIGRHs3d7eTJZwTQZZa2_image.png)

