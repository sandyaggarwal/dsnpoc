---
title: Add chatbot on a real customer website
slug: smM3-add-chatbot-on-a-real-customer-website
createdAt: Wed Mar 13 2024 13:18:54 GMT+0000 (Coordinated Universal Time)
updatedAt: Wed Mar 13 2024 13:55:34 GMT+0000 (Coordinated Universal Time)
---



> Before you begin check if you have appropriate schemas and datasets on your sandbox. There should be two schemas called: 
>
> **Demo System - Profile Schema for Stackchat Chatbot (Global v1.1) and Demo System - Event Schema for Stackchat Chatbot (Global v1.1)**
>
> and two appropriate datasets: 
>
> **Profile Dataset for Stackchat Chatbot (Global v1.1) and Demo System - Event Dataset for Stackchat Chatbot (Global v1.1).**
>
>  If you don't have the schemas please check the section at the bottom: How to install schemas required by chatbot 

###

## Configuration

Once you will go through the Quick Setup by selecting the External Website preset, you will have the Data Collection property ready. Everything what is needed is already there but you need to do some updates.

1. Open the Data Collection property that you are using with your website
2. Go to the Rules and find the one called "Initialize chatbot" -it is disabled by default

![](https://docs.adobedemo.com/~gitbook/image?url=https:%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MMLrO7TweNFMn8PgeVh%252Fuploads%252Fp9xFoLeKhLpfqk1VuivX%252Fimage.png%3Falt=media%26token=2b308ba1-6536-49fb-acef-25ce44c9dc87\&width=768\&dpr=4\&quality=100\&sign=20c4bc7f7d3607ab751e0ec2b048fe43519868609f51db259caca1f2b85a4515)

1. Select the rule and click "Enable". Click "Add to Library and Build" and wait until the library will be build

![](https://docs.adobedemo.com/~gitbook/image?url=https:%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MMLrO7TweNFMn8PgeVh%252Fuploads%252FP6X96swYewe7lcvTXmbC%252Fimage.png%3Falt=media%26token=495c5512-ae43-40e3-85bc-482b2a3cdebe\&width=768\&dpr=4\&quality=100\&sign=5012649dd0cdbafe5241aaf77bf23172bb1adacfa33114d88ace5adeee51c869)

1. After successful build you should see the chatbot on your page (refresh the page and wait few seconds)

![](https://docs.adobedemo.com/~gitbook/image?url=https:%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MMLrO7TweNFMn8PgeVh%252Fuploads%252FMtUN42LivPFMc0PCGZzk%252Fimage.png%3Falt=media%26token=4a0032d4-736f-4f5e-aaba-638fc1d711f9\&width=768\&dpr=4\&quality=100\&sign=0cb4fba4e9b00ee48c99a3fea0342c7a7d4f667c8203003004eb3f78645e6955)



![](https://docs.adobedemo.com/~gitbook/image?url=https:%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MMLrO7TweNFMn8PgeVh%252Fuploads%252FzqNE3kuCpmKhz4069apJ%252Fimage.png%3Falt=media%26token=8eef1315-cf5b-4d5c-af38-2f2def000eb5\&width=300\&dpr=4\&quality=100\&sign=d631f3e4b0fadc822fff9b2caa95426d17b64d9739d4f9850ddd229b6750016f)

If you see the events in the AEP profile but not in the Profile Viewer, open your builder project and make sure the bot.interaction filter is there. Also make sure it is placed above the Page View rule. If needed reorder the events.

## How to update the flow for your needs?

### **Retail**

There are few bot variables that you can update, they will be visible in the conversation after selection "I am looking for a gift". To update the values open your Data Collection property and switch to Data Elements section

![](https://docs.adobedemo.com/~gitbook/image?url=https:%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MMLrO7TweNFMn8PgeVh%252Fuploads%252FWZSZ5NcSxYMXHuipebHk%252Fimage.png%3Falt=media%26token=dab7001c-b974-45e4-afb3-80f90bcb71e0\&width=768\&dpr=4\&quality=100\&sign=ca707c76c1dff2cfc5c4e124a6a237268635466d25816c08ee56da31f3843864)

Bot - Proposed Product Image

Bot - Proposed Product Name

Bot - Proposed Product Url

![](https://docs.adobedemo.com/~gitbook/image?url=https:%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MMLrO7TweNFMn8PgeVh%252Fuploads%252FISQFBCL04GfKpTb5z4nE%252Fimage.png%3Falt=media%26token=36315a97-0b82-4750-94a7-cbd27dba475e\&width=768\&dpr=4\&quality=100\&sign=f110ecef4c7915566480a52e795f038bb725a8252e8bf6ebf01f496b10bf5529)















Please follow these for vertical specific details:

[Retail Bot Flow](https://dsndocs.adobe.com/docs/retail-bot-flow)&#x20;

[FSI Bot Flow](https://dsndocs.adobe.com/docs/fsi-bot-flow)

[Healthcare Bot Flow](https://dsndocs.adobe.com/docs/healthcare-bot-flow)

### Use other Verticals

By default the property was created with a retail bot attached but you can easily connect other vertical specific bots for FSI, Healthcare or Automotive.&#x20;

Go to you Data Collection property and switch to the Data Elements tab. Open the Bot - ID data element and update it according to your vertical



| Vertical         | Bot - ID Value     |
| ---------------- | ------------------ |
| Retail (default) | **ukxfhtgo41ty69** |
| FSI              | **cvyuzkbwew3oij** |
| Automotive       | **j72e2843ml1qek** |
| Healthcare       | **j3vzoz51l11ll0** |

Remember that after every change you need to rebuild your library. While saving the data element, make sure the library is selected in the top right corner and choose: Add to library and build

![](https://docs.adobedemo.com/~gitbook/image?url=https:%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MMLrO7TweNFMn8PgeVh%252Fuploads%252FcPsWsHJJvRnqetsLHhc9%252Fimage.png%3Falt=media%26token=c30b07b4-0a90-47c5-ba65-8dd09a0c486c\&width=768\&dpr=4\&quality=100\&sign=ba64d2bc4a54cc795ef3e3b10b04e16b371a1bad3825e523786084f197358aa5)

Within other verticals there are several data elements that can be also created to update the flow content:

&#x20;You can add two data elements with extension core and  type: Constant

![](https://docs.adobedemo.com/~gitbook/image?url=https:%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MMLrO7TweNFMn8PgeVh%252Fuploads%252FVDuxAXmOHiITVDs8iiV8%252Fimage.png%3Falt=media%26token=c4bc4cea-b746-4929-a915-7332fd70bb9e\&width=768\&dpr=4\&quality=100\&sign=65fb6f3edde7e0265f5e0a0e04330fbbc3c2f2e656877eb6933e2ad398a09c0d)

Bot - Card Name - will store the card name displayed later in the flow

&#x20;Bot - FSI JO Event ID - should store the event id which will be used in the chatbot flow.

### [Learn more about FSI flow](https://dsndocs.adobe.com/docs/fsi-bot-flow)

Bot - Proposed Car Image

Bot - Proposed Car Url

Bot - Proposed Car Name

![](https://docs.adobedemo.com/~gitbook/image?url=https:%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MMLrO7TweNFMn8PgeVh%252Fuploads%252FE6Cghjq5KEQhIKmlJ8Uv%252Fimage.png%3Falt=media%26token=6566b40e-e1bd-4a23-acda-74db1a259495\&width=768\&dpr=4\&quality=100\&sign=3dc4267eabceb63ae36c6a72f843f9bcf5f7b740dec8e01c7792a71f92c8da87)

### [Learn more about Healthcare flow](https://dsndocs.adobe.com/docs/healthcare-bot-flow)

### **Additional parameters that can be updated for all verticals**

We can also customise Bot Icon, Bot Name , other parameters. For this - Go to Rules. Click on **Page View **rule**. **Click on "**Initiate Bot**" action.

![](https://docs.adobedemo.com/~gitbook/image?url=https:%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-legacy-files%2Fo%2Fassets%252F-MMLrO7TweNFMn8PgeVh%252F-Mc8OOZT7FwgC2XjWJ3y%252F-Mc8P9LAQDPi7t4Fq-ZH%252Fimage.png%3Falt=media%26token=57527824-64bb-44f8-8a87-fd5f1588ff95\&width=768\&dpr=4\&quality=100\&sign=72187bbb511ea8a2d5a4553a968a597c386481e6bfce36d96ad2e7d4baa3442e)

![](https://docs.adobedemo.com/~gitbook/image?url=https:%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-legacy-files%2Fo%2Fassets%252F-MMLrO7TweNFMn8PgeVh%252F-Mc8OOZT7FwgC2XjWJ3y%252F-Mc8PF0t-roBIJEV11-X%252Fimage.png%3Falt=media%26token=53f6c199-c203-4556-9420-9108b02a47a5\&width=768\&dpr=4\&quality=100\&sign=e4441bfd1661419f7d56dbded2151cd7b65b4fdb396ca199823ab161c96886d1)

- Scroll to the bottom in the rule. We can see bot customisation parameters. It can be modified to match your client. Make sure to publish the changes.

![](https://docs.adobedemo.com/~gitbook/image?url=https:%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-legacy-files%2Fo%2Fassets%252F-MMLrO7TweNFMn8PgeVh%252F-Mc8OOZT7FwgC2XjWJ3y%252F-Mc8PM61UJqBKItMEGw1%252Fimage.png%3Falt=media%26token=42a76f64-a821-44d6-b91c-b8871e50edc7\&width=768\&dpr=4\&quality=100\&sign=6034f7ee9d01f48cae16fd13a5b6253a996c525be6ac46373322f95804069afd)

![](https://docs.adobedemo.com/~gitbook/image?url=https:%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-legacy-files%2Fo%2Fassets%252F-MMLrO7TweNFMn8PgeVh%252F-Mc8OOZT7FwgC2XjWJ3y%252F-Mc8P_e_zQnVotZ2ZLP3%252Fimage.png%3Falt=media%26token=8602e815-474c-4a43-968d-547d3e6f8ef2\&width=768\&dpr=4\&quality=100\&sign=e98851b15a5cb0f612a316a90a3d21a9c0479dca5361daf599de0cbce295db83)

## How to install schemas required by chatbot

Go to quick setup and from the advenced section in AEP column, select "Chatbots" and "Retail". Proceed as previously. After a while you should see the required schemas in your sandbox.



![](https://docs.adobedemo.com/~gitbook/image?url=https:%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MMLrO7TweNFMn8PgeVh%252Fuploads%252FFUwMmiJlJHxO2qLUOEmF%252Fimage.png%3Falt=media%26token=595c7d22-247b-48d7-94bd-74794796cb88\&width=300\&dpr=4\&quality=100\&sign=b8d66cf7548ccfe1c26fcc054e19a51783f1e8ff732e34f05172a0af9e69e9c4)

