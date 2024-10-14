---
title: How to use AEP Audiences in Target using Destinations
slug: zWz4-how-to-use-aep-sandbox-segments-in-target-using-destinations
createdAt: Mon Nov 13 2023 14:38:38 GMT+0000 (Coordinated Universal Time)
updatedAt: Tue Jun 04 2024 12:56:13 GMT+0000 (Coordinated Universal Time)
---

### PREREQUISITES

1. Make sure you have created the Audience in AEP
2. Have a Data Collection property connected to the website/mobile app

- 1) Go to AEP UI, switch to your sandbox. Select Destinations from the navigation on the left. Switch to Catalog tab
- ![](../../assets/DGNE-S5fii4ih0wJE93Ui_image.png)

* 2\. Search for Target. Click "Set up"
* ![](../../assets/PNMMMAD2lp7P90ub8Bdzc_image.png)

- 3\. Click on "Connect to destination"
- ![](../../assets/RfgHoKqXgvsqz9hlNE915_image.png)

* 4\. Provide the connection name. Make it unique as every Launch property needs its own connection. As Datastream ID search for the same name as you used while going through quick-setup property. If you don't see it on the list follow
* ![](../../assets/DlKgaM0ZdVHTJESzhY1X__image.png)

- 5\. 5. Select the policy you will use, if you don't know which one to select, select all. Click "Next"
- ![](../../assets/49HW3Ql0U_qrKFuM0PSPQ_image.png)

* 6\. Select the segment you want to see in Target. Click Next
* ![](../../assets/GbAnw9Lt0PC9idhvCRJsS_image.png)

- 7\. Check the summary and click Next
- ![](../../assets/ti2emzJq_GTcwxcBgrCyp_image.png)

* 8\. Click "Finish".&#x20;
* ![](../../assets/AahvCLQILK-2_Cei2chYC_image.png)

- 9\. Log in to Target, switch to Audiences tab. You should see your segment there.
-

## TROUBLESHOOTING

### I can't find my property listed as datastream.

- 1. Go to Data collection -->Datastreams.&#x20;
-

* 2\. Find your datastream by searching for the same name as you used in Quick Setup. Open it. Click on the Development Environment
*

- 3\. Scroll down to see the Adobe Experience Platform settings.&#x20;
-

* 4.Make sure the "Personalization Destinations" checkbox is selected.
*

