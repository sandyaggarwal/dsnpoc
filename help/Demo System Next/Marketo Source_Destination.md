---
title: Marketo Source/Destination
slug: zpOl-configuring-marketo
createdAt: Wed Nov 15 2023 13:45:38 GMT+0000 (Coordinated Universal Time)
updatedAt: Wed Nov 15 2023 14:02:50 GMT+0000 (Coordinated Universal Time)
---

Demo System Next allows you to configure the Marketo source/destination connections automatically. After that you will be able to see the profiles/companies/opportunities imported from Marketo and SalesForce. You will be also able to create audiences and send them to this destination.

## Prerequisites

1. Your org needs to be enabled to B2B

&#x20;    2\. Your Marketo instance needs to be added in Demo System Next database. For Adobe Demo System Shared and Adobe Demo System Individual we have 2 instances already provided. Reach out to #demo-system-next slack channel to get access to those. The shared Marketo demo instance is connected and synced with Salesforce CRM.If you need to access it, click [here](https://wiki.corp.adobe.com/display/demosystem/Marketo+Shared+instance+for+Sales+Velocity+Demo+System+org#MarketoSharedinstanceforSalesVelocityDemoSystemorg-SharedSalesforceDemoaccount) to get the credentials.

&#x20;    For any other Marketo instance plase contact us as well. The automation is possible with any Marketo instance.

## Instructions

Go to [Quick Setup](https://dsn.adobe.com/quick-setup) and select the environment/sandbox.

Select preset \`B2B RTCDP + Marketo\` and click start in top right

![](../../assets/C8m-tEpoeb9_34S75xGYK_image.png)

Provide title and select the Marketo instance for configuration

![](../../assets/NV5eEWZG43yVmprXfozZ8_image.png)

Click "Start" and wait for the results.

After you run the configuration, Marketo source connection will be created with source dataflows. Go to AEP -> Sources and check your configuration

![](../../assets/Z7MqCj0APSMO8AGSMuj27_image.png)

![](../../assets/c2EdveEjmdOAsR06QLU8F_image.png)

### Expected latency of Marketo data on Platform

The following table outlines the expected latency for bringing Marketo data into Adobe Experience Platform, based on the nature of ingestion and the desired destination:

| **Destination expected latency** |              |
| -------------------------------- | ------------ |
| Real-time Customer Profile       | < 1 minute   |
| Data Lake                        | < 60 minutes |

### Validation steps

In AEP, Source Account should be created, Dataflow runs should be successful and data should be ingested into the sandbox

Go to accounts in AEP, select "Source -> Demo System - Marketo Engage" and for example, provide "Account ID -> 4.mkto\_org"

![](../../assets/LfICgO1Glmmmck8GhZh-b_image.png)

Account should be present. Now, click on the account details, click attributes to view account attributes, click people to see the individual profiles linked with the account

![](../../assets/Rsy-2ccu1v8PQ1TcD3REv_image.png)

![](../../assets/U_oJAwDZTTknje5M1qN6p_image.png)

![](../../assets/XWRUxjumaA2-Wi3oWUav8_image.png)

