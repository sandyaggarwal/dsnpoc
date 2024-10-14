---
title: Manual Updates required for journeys
slug: ISxD-manual-updates-required-for-retail-vertical-journeys
createdAt: Mon Oct 07 2024 06:42:17 GMT+0000 (Coordinated Universal Time)
updatedAt: Mon Oct 07 2024 06:43:33 GMT+0000 (Coordinated Universal Time)
---

Add Contextual attributes to the journeys.&#x20;

Open Experience platform: <https://experience.adobe.com/>. Click on three dots, next to org name. Open "Journey Optimizer"

![](https://docs.adobedemo.com/~gitbook/image?url=https%3A%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MMLrO7TweNFMn8PgeVh%252Fuploads%252FP73MeJjRMy4WCgPRcLO8%252FScreenshot%25202021-10-19%2520at%25206.36.49%2520PM.png%3Falt%3Dmedia%26token%3Df7e572f9-1cba-49c7-bd56-7ecabf541172\&width=768\&dpr=4\&quality=100\&sign=7904093e\&sv=1)



Select the sandbox, and Click on "Journeys" in the left navigation



![](https://docs.adobedemo.com/~gitbook/image?url=https%3A%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MMLrO7TweNFMn8PgeVh%252Fuploads%252FsgdXl37LjT7UHLzySsAQ%252FScreenshot%25202021-10-19%2520at%25206.42.22%2520PM.png%3Falt%3Dmedia%26token%3D07f6404b-8946-44c0-afae-647dc8899a65\&width=300\&dpr=4\&quality=100\&sign=bec1c166\&sv=1)

For Example, go to Journey's "**Luma Website Checkout Abandoners**", "**Luma - Website - Purchase Confirmation**"

Click on the "Message" and open the message from right rail

![](https://docs.adobedemo.com/~gitbook/image?url=https%3A%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MMLrO7TweNFMn8PgeVh%252Fuploads%252FvA1nlx13q0LDQfaG9Mqr%252FScreenshot%25202021-10-20%2520at%252012.41.12%2520PM.png%3Falt%3Dmedia%26token%3Df8e96ded-51a8-4308-aa08-6d2a23776d60\&width=768\&dpr=4\&quality=100\&sign=b316228c\&sv=1)

Open "Email Designer" and click in the left navigation "Contextual attributes". Select "Context" -> "Journey Orchestration" -> "Events" -> "Luma\_Website\_Checkout" -> "ProductListItems". We are doing this since journey API's are able to link EventID (Journey Contextual Data) with message and we have do it manually right now.

![](https://docs.adobedemo.com/~gitbook/image?url=https%3A%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MMLrO7TweNFMn8PgeVh%252Fuploads%252FyJ04SytWTe7YtnMotMsu%252FScreenshot%25202021-10-20%2520at%252012.54.32%2520PM.png%3Falt%3Dmedia%26token%3D9f03b114-e0a6-4bdf-a0a0-a786fcebca01\&width=768\&dpr=4\&quality=100\&sign=c8271ca1\&sv=1)

![](https://docs.adobedemo.com/~gitbook/image?url=https%3A%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MMLrO7TweNFMn8PgeVh%252Fuploads%252FJgBcrd9yCxIfPoCbEHCy%252FScreenshot%25202021-10-20%2520at%25203.13.31%2520PM.png%3Falt%3Dmedia%26token%3D44ac0396-7b64-4c82-b3a6-3177647318c7\&width=768\&dpr=4\&quality=100\&sign=da2f2da\&sv=1)

After making above changes, save and publish the message

![](https://docs.adobedemo.com/~gitbook/image?url=https%3A%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MMLrO7TweNFMn8PgeVh%252Fuploads%252FKipGdnzUWFwq5XH5nIkh%252FScreenshot%25202021-10-20%2520at%25203.20.53%2520PM.png%3Falt%3Dmedia%26token%3D330a11c1-07d7-4ed7-8978-ab2ec77cc631\&width=768\&dpr=4\&quality=100\&sign=484d0083\&sv=1)

Repeat the above steps for "**Luma - Website - Purchase Confirmation**" journey and message "Luma - Order Confirmation" linked with the journey.
