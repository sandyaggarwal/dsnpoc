---
title: Retail - send data to AEP using website
slug: a-OJ-retail
createdAt: Thu Oct 19 2023 14:59:05 GMT+0000 (Coordinated Universal Time)
updatedAt: Fri Oct 20 2023 09:49:20 GMT+0000 (Coordinated Universal Time)
---

1 Go to[ https://dsn.adobe.com](https://dsn.adobe.com)

2\. Find your workspace and open your website project (If you don't have one check the [Preparing Demo Environment](<../Demo System Next/Preparing Demo Environment.md>) section) by clicking "Run" in the top right corner of your website project.

![](../../assets/i4qdxLqnaIdzRMrj0hEw2_image.png)

3\. Notice the small icon in the top left corner. If you click on it a panel with profile details will show up. We will call this panel in the docs "Profile Viewer"

![](https://2470783510-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MMLrO7TweNFMn8PgeVh%2Fuploads%2FKtYlC63EkNBrGkE4XRxL%2Fimage.png?alt=media\&token=1120155c-387e-4fa0-8fe7-8c7cb33ecfa2)

Profile Viewer reads real data from AEP. You should be able to preview changes while browsing the website, signing-in etc.

:::hint{type="info"}
To learn more about Profile Viewer and ability to modify its fields and displayed values check this section: [Profile Viewer](<../Demo System Next/Profile Viewer.md>)
:::

To send data to AEP we can do following actions

1. Start with an anonymous profile on a website. Profile viewer should have no data expect of Experience Cloud ID which is an anonymous user identifier. You can use this ID to search for the profile in AEP UI.
2. Collect experience events while browsing products/adding them to cart/making purchase/register to webinars etc.

**Below example is for a retail project, but for other verticals the mechanism is the same.**

![](../../assets/EGj0ZPBc1XnGjhNY6PBHC_image.png)

