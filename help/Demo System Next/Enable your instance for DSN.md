---
title: Enable your instance for DSN
slug: gODz-enable-your-instance-for-dsn
createdAt: Thu Aug 24 2023 09:38:22 GMT+0000 (Coordinated Universal Time)
updatedAt: Thu Nov 30 2023 10:46:05 GMT+0000 (Coordinated Universal Time)
---

​In order to use Demo System Next integration with your Adobe Commerce instance, you need to follow 3 steps:

1. Enable token-based access to API
2. Set up service token to be used by DSN integration
3. Register you instance details in DSN

### Enable token-based API access

-

  1. Open your Adobe Commerce instance Admin Panel and sign in.
  2. From side-navigation select Stores > Configuration
  3. In the Configuration view, navigate to Services > OAuth > Consumer Settings
  4. Set `Allow OAuth Access Tokens to be used as standalone Bearer tokens` to `Yes`
  5. Click `Save Config` button in the top-right corner.
- ![](../../assets/hjvkkIpZRf68RG-kda3Wu_image.png)

  ![](../../assets/O3XyOSGXcV0gQC6lOf0qn_image.png)

### Set up service token

- 1. Open your Adobe Commerce instance Admin Panel and sign in.
  2. From side-navigation select Settings > Extensions > Integrations


- ![](../../assets/idvr3DHaqQrqWxMN3GRSv_image.png)

* 3\. In the Integrations view click `Add New Integration`
* ![](../../assets/jgBjFmKBr8kLdtutUo0f7_image.png)

- 4\. In Integration Info section fill in the name, eg. `Demo System Next API` and your admin panel password. Don't save this integration yet. Switch to `API` tab in the left-side menu.
- ![](../../assets/1gJB6dB0oKJ4SeXMoV-Co_image.png)

* 5\. In API tab change `Resource Access` dropdown option to `All`.&#x20;
  *\* You can try to set more refined permissions, however the list of required permissions changes often, so you may need to maintain it.*
* ![](../../assets/JtbPjmeZD7hxKdPCcUa3i_image.png)

- 6\. Click arrow icon next to `Save` button and select `Save & Activate`
- ![](../../assets/2mRyEthX7gRI-wzRRWIWY_image.png)

* 7\. On the next page click `Allow`
* ![](../../assets/eYSt9SdsdT6-F34BsJqmm_image.png)

- 8\. On the summary screen you will be presented with several properties. Copy value of `Access Token`. You will need to provide it to your DSN integration later.
  If you lose this value, you can preview it by clicking `Edit` icon next to your integration on Integrations view list.
- ![](../../assets/66oQPnlPa6uRzm4hAjHMZ_image.png)

### Register instance in DSN

- 1\. Go to&#x20;

  <https://dsn.adobe.com/tools/commerce-admin>

  2\. Click "Add" button
- ![](../../assets/mhxOAJHzA9eZt5Wstk0Zb_image.png)



- 3\. Fill in the form:

  - Name - friendly instsance name that will be visible within DSN. Try to keep it short.
  - Instance URL - base address of your instance (not admin panel)
  - Admin Panel URL - link to admin panel for your convenience
  - Access Token - integration value from previous section

  4\. Click `Save`. This will try to establish connection to your instance. If you completed setup steps from two previous sections it should validate successfully. Your instance will appear on the list and it will show up as an option in project integrations.
- ![](../../assets/PUIBbMd6Fmn5kiz6tdt-5_image.png)

