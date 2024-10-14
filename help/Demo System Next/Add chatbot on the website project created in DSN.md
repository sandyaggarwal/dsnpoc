---
title: Add chatbot on the website project created in DSN
slug: -gdu-add-chatbot-on-the-website-project-created-in-dsn
createdAt: Wed Mar 13 2024 13:31:54 GMT+0000 (Coordinated Universal Time)
updatedAt: Wed Mar 13 2024 19:02:10 GMT+0000 (Coordinated Universal Time)
---

> Before you begin check if you have appropriate schemas and datasets on your sandbox. There should be two schemas called: 
>
> **Demo System - Profile Schema for Stackchat Chatbot (Global v1.1) and Demo System - Event Schema for Stackchat Chatbot (Global v1.1) **
>
> and two appropriate datasets: 
>
> **Profile Dataset for Stackchat Chatbot (Global v1.1) and Demo System - Event Dataset for Stackchat Chatbot (Global v1.1)**
>
> . If you don't have the schemas please check the section at the bottom: How to install schemas required by chatbot

Any website project can use bots. They are disabled by default. To enable bot you need to enable it.

1. Open your website project and switch to the Integrations tab

![](https://docs.adobedemo.com/~gitbook/image?url=https:%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MMLrO7TweNFMn8PgeVh%252Fuploads%252FcYWUeSAYWmMcFD3IqEuC%252Fimage.png%3Falt=media%26token=44d24ea8-6386-4d12-a8bf-05e691cd2001\&width=768\&dpr=4\&quality=100\&sign=b40fa3589501aead77f790ae1826db0d9915248558e8890e71b23c9a0172cfe8)

Click "Configure" on the Chat Bot rectangle. By default as you can see the chatbot is disabled



![](https://docs.adobedemo.com/~gitbook/image?url=https:%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MMLrO7TweNFMn8PgeVh%252Fuploads%252Fhz4YKpx8zFfLmOWELEg8%252Fimage.png%3Falt=media%26token=23aae13b-d959-47ae-a5b7-06de3f1c22be\&width=300\&dpr=4\&quality=100\&sign=a8ad257361abc6be58c7a0efb37aad7247518c2ebfc3d64bc725096c615f44f9)

Switch to Pre-defined and select the vertical you want to use



After the selection you will have an option to modify few values used by the bot to match your customer website products or your scenario.

![](../../assets/Pz2NeUk4tMkdBRzBGky_S_image.png)

Retail - [Learn more about the Retail flow](https://dsndocs.adobe.com/docs/retail-bot-flow)



![](../../assets/QdTV1fnpkEP3WsrXe9ZHm_image.png)

FSI - [Learn more about the FSI flow](https://dsndocs.adobe.com/docs/fsi-bot-flow)



![](../../assets/MM-BH_PQNjijl6S4-OzEd_image.png)

Healthcare - [Learn more about the Healthcare flow](https://dsndocs.adobe.com/docs/healthcare-bot-flow)



Click "Save"

![](../../assets/H4yg3hAInwi_CkkWvR2hL_image.png)

If you refresh the page you should see the chatbot icon in the bottom right corner

![](https://docs.adobedemo.com/~gitbook/image?url=https:%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MMLrO7TweNFMn8PgeVh%252Fuploads%252FccNMq3CxoPAFwHtKGV1o%252Fimage.png%3Falt=media%26token=4f52a9aa-36b4-47fc-a440-ee976befad97\&width=768\&dpr=4\&quality=100\&sign=6b9a5eefbbc24dc478edf2bb7fa2e7e3ed3b639cddf36fe74f06bde7893d21ff)

All interactions should be visible in the profile in AEP, on the events tab as bot.interactions.&#x20;

If you see the events in the AEP profile but not in the Profile Viewer, open your builder project and make sure the bot.interaction filter is there. Also make sure it is placed above the Page View rule. If needed reorder the events.



![](https://docs.adobedemo.com/~gitbook/image?url=https:%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MMLrO7TweNFMn8PgeVh%252Fuploads%252F8vT5GYQcNYOxmjH7E9Qf%252Fimage.png%3Falt=media%26token=e0977a1f-1197-426c-abe2-baf90c288e29\&width=300\&dpr=4\&quality=100\&sign=5e2267a86a4c73777e98f8d448fa04afa79f9631839cb3c488f17260beeb535f)

### How to install schemas required by chatbot

Go to quick setup and from the advenced section in AEP column, select "Chatbots" and "Retail". Proceed as previously. After a while you should see the required schemas in your sandbox.



![](https://docs.adobedemo.com/~gitbook/image?url=https:%2F%2F3295630118-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MMLrO7TweNFMn8PgeVh%252Fuploads%252FFUwMmiJlJHxO2qLUOEmF%252Fimage.png%3Falt=media%26token=595c7d22-247b-48d7-94bd-74794796cb88\&width=300\&dpr=4\&quality=100\&sign=b8d66cf7548ccfe1c26fcc054e19a51783f1e8ff732e34f05172a0af9e69e9c4)

