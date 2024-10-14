---
title: How to set up external website demo?
slug: AtrR-how-to-set-up-external-website-demo
createdAt: Tue Oct 24 2023 11:48:30 GMT+0000 (Coordinated Universal Time)
updatedAt: Tue Oct 24 2023 13:50:47 GMT+0000 (Coordinated Universal Time)
---

:::hint{type="info"}
This way of demoing should be used only for non-DSN web pages. If you have build the website with DSN, please read [Retail demo environment](<../Demo System Next/Retail demo environment.md>) to connect your Data Collection property.
:::

## Instructions

This process consists of 4 stages:

1. Creating a Launch property through Demo System Dashboard
2. Injecting Launch property into the website
3. Modifying a Launch property to match your scenario
4. Updating Profile Viewer fields to match your scenario

We will use <https://us.coca-cola.com/> as an example.

:::hint{type="warning"}
You will need Adobe Experience Platform Debugger in order to do this demo. You can download the plugin from here:

Chrome: [AEP Debugger for Chrome](https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob?hl=en)

Firefox: [AEP Debugger for Firefox](https://addons.mozilla.org/en-US/firefox/addon/adobe-experience-platform-dbg/)
:::

## 1 Creating Data Collection property

- Go to the environments section in DSN <https://dsn.adobe.com/environments> and the sandbox you will be using for your demonstration. Click "Quick Setup" from the navigation on the right.
- ![](../../assets/Vmzz5h2pZfJGlvZmzVyS-_image.png)

* On the quick setup screen, Select the **"Retail - Basic (External Website)"** Preset. Click "Next"
* ![](../../assets/XPbqYjUQlwQIRrQZNCbcV_image.png)

- Enter a configuration name (e.g. your customer's name), this will be used as a name for your Launch property. Please provide a DR number if this is a demo for customer. Click "Start" and wait few minutes
- ![](../../assets/grlYnt4Cj5hvbmJ9Jcinh_image.png)

  ![](../../assets/F6_sv70j4Avogwvvk2Dul_image.png)



- You can click on the Data Collection property link to go to Data Collection as it will be needed in the next step
-

## Add Data Collection property to the website

- Go to experience.adobe.com, switch to Data Collection. Make sure you are using the right org and search for the Tag with the name you provided in the configuration above
- ![](../../assets/Q57cW1HHaHltVP8M2S--W_image.png)

* First, you'll need to get the embed code of your Launch property: go to&#x20;

  **Environments**, click the package icon in the **Development **row and copy the whole \<script src="//assets.adobedtm.com/... value.
* ![](../../assets/sHIoZXtx8dS6SlhcL-yyL_image.png)

  ![](../../assets/UjYTFLPjMKOlwJhJiP4bV_image.png)



- Navigate to your customer website, in this case it is <https://us.coca-cola.com/> Open the AEP Debugger Plugin. Make sure that the message at the bottom says: Connected and the dot has green color. If it is not, do not close the debugger but refresh the page in the background.
- ![](../../assets/prKnRTsY4tesIL-Ux_hDo_image.png)

* Click the Experience Platform Tags section and switch to the Configurations tab. Click **Add new embed code**button. Paste the embed code into the text field. "Apply" and Click "Save".&#x20;

  **If the page already has a Tag (and Coca Cola website has one already), the add new functionality won't work - use replace option instead of add.**
* &#x20;

  ![](../../assets/GE9AKPbZ6Hu3p6W80AaWV_image.png)

  If the page already has a Tag, use replace option instead of add.

:::hint{type="info"}
Keep the Adobe Experience Debugger plugin minimized. Do not close it as then the ingestion won't work.
:::



- The page in main browser window should reload and you should see the small AEP icon in top-left corner.
- ![](../../assets/hk2iu6PIk5YETrBhcDqpF_image.png)

* Click the AEP icon in the top-left corner, it should open the Profile Viewer component. You are ready to go!
* ![](../../assets/nQYNVpX_mCCafohi70cgv_image.png)

## Send Experience Events (Page Views) to AEP

:::hint{type="info"}
Page Views experiene events will work by default on every page. You can observe them in Profile Viewer Events tab, while you are browsing the website.
:::

- Click few pages, the events panel will start filling with page view data
- ![](../../assets/KQjjFCtBXK4thtNzrUUUn_image.png)

## Simulate Registration on the web page

You have several ways to simulate Registration on a customer web page. In this scenario we will use the simplest one. If you would like to learn more about different possibilities to authenticate on a web page please read  "[Registration/Sign In]()" section.

- Open profile viewer and expand "Utitilies" section on the "Profile" tab
- ![](../../assets/-92lwzuQiS7OWOo7-6-Pe_image.png)

* Click the "Register" Action a pop up will show up
* ![](../../assets/-9AE2rMKnGS5JuHXeDMeZ_image.png)

- Enter the email, first name and last name. Click "Submit". Request will be send to AEP with a new profile information. If this profile already exists in AEP, both profiles will be merged. (You can also use login for existing profiles)
- ![](../../assets/t3rTGcR4M2QM3HWmtwQ2r_image.png)

* After few seconds the profile details should be visible in the profile viewer.
* ![](../../assets/PYHPX8PZWdOPi3EUWbk3C_image.png)

## Review and Modify Launch property

In the example below we will show you how to customize the Launch property to track Product Views. For more scenarios please check the "[Features]()" section.

### Adding Product Views Events.

If you want you can hide page views and focus only on product views (How to do that you will learn in [this section]() )but we need to prepare the product views experience events first.

- Find your Data collection property. Go to the Rules and find the "Product View" rule
- ![](../../assets/d9W-cwx19yUG2IIpoLP4Y_image.png)

* Open the "Product Pages URL" condition.

  You will need to update the paths to match your website so that the rule is triggered on product pages.&#x20;
* ![](../../assets/Aci8a2a9wwJp3S6P33jKZ_image.png)

- Go to the coca-cola page and try to make a decision what might be a product in case of your story and this page.&#x20;

  For the purpose of this exercise the products will be items when you click "our products" like <https://us.coca-cola.com/products/coca-cola/original> or <https://us.coca-cola.com/products/coca-cola-flavors/cherry>. Common pattern for this urls is the word: "products" in the URL. Always search for the pattern that is common, it can be "shop" or "items", analyze your product urls
- ![](../../assets/ohSTIeXdqAUXHxhCTwZP2_image.png)

* We need to update the path equals but in this case the default value already matches the product pages so leave it as it is. On the screenshots on the left you will see another examples for cases like "shop" and "items".&#x20;

  Always remember to check the "Regex" switch and add .\* before and after your sentece. It will make the condition generic enought to match the url you want.
* ![](../../assets/oxyhdzkrgfee--XXZU0pl_image.png)

- You might need to modify the product image data element (Product Name will work on every page by default). In case of Coca-Cola page the image works by default but same pages requires modification and we will do that for practice.

  Identify the image which is a product image on your product page. In this case e.g. <https://us.coca-cola.com/products/coca-cola-flavors/cherry>
- ![](../../assets/uw85rsgJv6S2WHvnJ700X_image.png)

* The console will open with highlighted element. Right click on it and select "Copy"->"Copy Selector"
* ![](../../assets/lMYhGG4EQtvHcvxgDkgwk_image.png)

- Go back to Data Collection (launch) and find data element "Product - Image". Open it.
- ![](../../assets/b0k1xUUUfTII6luSMNKnn_image.png)

* From the dropdown "Extension" choose "Core"

  &#x20;From the dropdown "Data Element Type" choose "DOM Attribute".

  Paste the copied code in the "From the DOM element matching the CSS Selector" field and choose value "src". Remember to "Save and build the library"
* ![](../../assets/Rc78fcpKo3vzWkGzyAyLi_image.png)

- Refresh the coca cola page, you should see product view in the events tab with an image
- ![](../../assets/yrDDrQea-hfIztMyGya0i_image.png)

## Review and modify Profile Viewer fields using Experience Builder (optional)

You can modify the profile and events displayed in profile viewer. Read the following article to do the changes [Profile Viewer](<../Demo System Next/Profile Viewer.md>)
