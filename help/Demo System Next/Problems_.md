---
title: Problems?
slug: xCQJ-problems
createdAt: Wed Nov 15 2023 09:45:20 GMT+0000 (Coordinated Universal Time)
updatedAt: Tue Feb 20 2024 10:44:02 GMT+0000 (Coordinated Universal Time)
---



## I can't see my audiences in profile viewer panel

If the segments are visible in the AEP UI but not in profile viewer, you need to check the filter set up in profile viewer. Open your project and switch to "Profile Viewer" tab. Scroll down to the "Segments" section and make sure the filter there matches your segmnet names or remove the filter to see all segments

![](../../assets/y1zuXHEInRwMMD46S-PcL_image.png)

## I can't see the sandbox I want to work with in quick setup

If you can see the org in <https://dsn.adobe.com/environments> but you don't see your sandbox, please contact the admin.&#x20;

Click on the i icon next to "Need access" message and write to one of the people mentioned there.

![](../../assets/zpWS59e4lkeznO6wGAVe7_image.png)

If you can't see your org please contact us on #demo-system-next channel



## After the app was installed I am getting information about "Untrusted Enterprise Developer"

The app is signed with an official Adobe enterprise certificate but by default, iOS will not treat it as trusted. To add it to the list of trusted certificates go to:

**iOS Settings -> General -> Device Management -> Adobe Systems Inc.**

and click “Trust Adobe Systems Inc.” You only need to do it once on given device.



