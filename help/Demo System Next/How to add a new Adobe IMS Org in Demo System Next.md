---
title: How to add a new Adobe IMS Org in Demo System Next
slug: dWD9-how-to
createdAt: Mon Feb 12 2024 21:51:16 GMT+0000 (Coordinated Universal Time)
updatedAt: Fri Feb 16 2024 16:47:55 GMT+0000 (Coordinated Universal Time)
---

This page describes step-by-step the process of adding a new Adobe IMS organization in Demo System Next.&#x20;

### Prerequisites

- You need to be the *System Administrator* of your Adobe IMS organization



### Key Steps

To add your Adobe IMS Organization in Demo System Next, you will need to perform the following key steps:

1. Create an AEP Product Profile and a Role with the required permissions
2. Create a new API Project in the Adobe Developer Console
3. Create a new IMS Org in the Demo System Next
4. Add AEP Sandboxes to your Environments list



### Step 1: Create an AEP Product Profile and a Role with the required permissions



- 1\. Open the [Adobe Admin Console ](https://adminconsole.adobe.com/)and click on **Products **in the top menu
-

  ![](../../assets/2cJGW9GOu3yyo2v_7ldkQ_cleanshot-2024-02-16-at-174605.png)

* 2\. Click on **Adobe Experience Platform**
*

  ![](../../assets/9_xzoHTbkfVDlbfgkXZQu_cleanshot-2024-02-16-at-160155.png)

- 3\. Create a new Product Profile `Demo System Next API Access - AEP` by clicking on **New Profile**
-

  ![](../../assets/OPWJqK-cgYC9zJ4GJ7mGa_cleanshot-2024-02-16-at-161923.png)

* 4\. Open the [Experience Cloud Home](https://experience.adobe.com/) and click on **Permissions**
*

  ![](../../assets/Fq9IDaWqdFHaeDhLH0uaM_cleanshot-2024-02-16-at-162046.png)

- 5\. Click on the **Create role** button and enter the following details:

  - Name: `Demo System Next API Access - AEP`
  - Description: `This profile groups all sandboxes that should be accessible by Demo System Next API`
-

  ![](../../assets/616r33oLlJF962bRVN95a_cleanshot-2024-02-16-at-174658.png)

* 6\. **Edit** the Role permission and add all sandboxes that you need to connect to Demo System Next with necessary permissions to manage AEP resources through the APIs e.g. *Manage Schemas*
*

  ![](../../assets/sW5YCP9jejMCQLlc2Ac5F_cleanshot-2024-02-16-at-162648.png)

You have now configured the AEP Product Profile and the required Role permissions.



### Step 2: Create a new API Project in the Adobe Developer Console

- 1\. Open the [Adobe Developer Console ](https://developer.adobe.com/console/projects)project view and click on **Create new project**
-

  ![](../../assets/QLFG0q8AuWTZRYGzGPsAv_cleanshot-2024-02-16-at-163429.png)

* 2\. **Edit** the project to set the project Title to:

  &#x20;`Demo System Next`
*

  ![](../../assets/OnE_OOAEK01AMhYhNFGZg_cleanshot-2024-02-16-at-163659.png)

- 3\. Add the following APIs to the project using the Product Profile `Demo System Next API Access - AEP`:

  - `Experience Platform API`
  - `Experience Platform Launch API`
  - `Adobe Journey Optimizer`
  - `Privacy Service API`
  - `Places`
  - `Assurance API`
  - `Adobe Target`
  - `Customer Journey Analytics`
-

  ![](../../assets/mWsAWehAjZhxdagV_lARH_cleanshot-2024-02-16-at-164401.png)

* 4\. Click on **OAuth Server-to-Server** in the left menu and save the following credential details for later:

  - `Credential Name`
  - `Client ID`
  - `Client Secret`
  - `Technical Account ID`
  - `Scopes`
*

  ![](../../assets/bjG-Zi1DPQxqgI1TodUGb_cleanshot-2024-02-16-at-164900.png)

Your Developer project is now ready for the Demo System Next integration.



### Step 3: Create a new IMS Org in Demo System Next&#x20;

- 1\. Open [Demo System Next Tools](https://dsn.adobe.com/tools) and click on **IMS Org Admin**
-

  ![](../../assets/12-18W484VVjgOcOZy8Wu_cleanshot-2024-02-16-at-165312.png)

* 2\. Click on **Add Org**&#x20;
*

  ![](../../assets/cFPHrOxAHtrzg9FIImkP3_cleanshot-2024-02-16-at-165416.png)

- 3\. Enter the following details and click on the **Save** button:

  - `IMS Org ID`
  - `Name`
  - `Tenant ID`
  - `Region`
-

  ![](../../assets/gHf5O_241mUkLr_kuL9IK_cleanshot-2024-02-16-at-165553.png)

* 4\. Click on the **Actions **button
*

  ![](../../assets/2ymQh0sZ67CpeKXZQSDvp_cleanshot-2024-02-16-at-165840.png)

- 5\. Enter the following Credential details copied earlier from the Adobe Developer Console and click on the **Save **button:

  - `Client ID`
  - `Client Secret`
  - `Technical Account ID`
  - `Scopes`


-

  ![](../../assets/VhbY7feigBEFfzQl-e9ov_cleanshot-2024-02-16-at-170025.png)



Your IMS Org has been added to Demo System Next. You can continue in the Environment Admin section to add AEP sandboxes to your [Environments list](https://dsn.adobe.com/environments).



### Step 4: Add AEP Sandboxes to your Environments list

- 1\. Go to [**Environments Admin**](https://dsn.adobe.com/tools/environment-admin)** **using the left menu. Select an IMS Org, Select your user then click on **+Assign**&#x20;
-

  ![](../../assets/0k2ULy7T6t8b4fiHt_MXC_cleanshot-2024-02-16-at-172013.png)

* 2\. Enter the AEP Sandbox name and click on the **Confirm **button
*

  ![](../../assets/8yl3eLsHZLSc3F_1V_-vj_cleanshot-2024-02-16-at-172509.png)

- 3\. You can now use [DSN Quick Setup ](https://dsn.adobe.com/quick-setup)to deploy a new industry preset configuration on your AEP sandbox
-

  ![](../../assets/rkFKJAbME8rp3cI_2y7bQ_cleanshot-2024-02-16-at-172719.png)

Congratulations 🎉, you have successfully onboarded a new Adobe IMS Org in Demo System Next and configured your AEP sandbox with an industry preset using the Quick Setup.



### Troubleshooting

If you face an issue during the configuration of your AEP sandbox in [Quick Setup](https://dsn.adobe.com/quick-setup), you should verify that the `Demo System Next` API Credential has been added to the AEP Permission API Credentials:

![](../../assets/v25tXZicDBYHMmCj-GuQ3_cleanshot-2024-02-16-at-173429.png)



