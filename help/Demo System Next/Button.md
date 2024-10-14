---
title: Button
slug: fPOFBO_Swk6IPjSK9tdoP
createdAt: Thu Oct 26 2023 11:51:05 GMT+0000 (Coordinated Universal Time)
updatedAt: Tue Nov 28 2023 12:50:30 GMT+0000 (Coordinated Universal Time)
---

The **Button **module allows you display a button with specified label and visual variant. Can trigger launch events or call a request to a webhook.

![](../../assets/0OviGPXmYk2HNE6dD1w_H_button.png)

## Methods of event triggering

- **Event Type**

  You can specify the name of the event that will be used to trigger Data Collection Rules
- **Webhook**

  You can choose to additionally send a request to a chosen URL when trigger an even using the button. The webhook request will contain data gathered on the website during the current session.
- **Custom Data**

  As an addition you can add extra data as an object to the data that is being sent with the event/webhook.

## Module configuration

### General settings

| **Property**     | **Description**                                                                                                  | **Default**                                                          |
| ---------------- | ---------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------- |
| **Hide title**   | Indicates whether the module title above the module content should be hidden or not                              | true                                                                 |
| **Title**        | The name of the module, displayed above the module content                                                       | Button                                                               |
| **Description**  | The description of the module, displayed as a tooltip after clicking on the info icon next to the module's title | A button triggering launch events or calling a request to a webhook. |
| **Button label** | The label of the button                                                                                          | Click me                                                             |

### Appearance settings

| **Property**  | **Description**                                                                                                    | **Default** |
| ------------- | ------------------------------------------------------------------------------------------------------------------ | ----------- |
| **Variant**   | A visual variant of the button. Can be one of the following: *Primary, Accent, Secondary, Negative*                | Primary     |
| **Type**      | You can choose whether the button is filled with the primary color inside or just outlined with the primary color. | fill        |
| **Alignment** | Horizontal alignment of the Button in the modules list.                                                            | Left        |

### Actions settings

| **Property**      | **Description**                                                                                                                                                                                          | **Default**     |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------- |
| **Event type**    | Type (name) of browser JavaScript event to send. Used to trigger Data Collection Rules.                                                                                                                  | --              |
| **Webhook URL**   | URL to send a request to on click. Request will contain all data gathered on site                                                                                                                        | --              |
| **Custom data**   | Valid JavaScript object with properties to add to dataLayer and webhooks on click. Can be used to set properties that don't have visual components on the site, eg. `{"enrollment.selectedPlan": "ppo"}` | {}              |
| **Delay**         | A number of milliseconds to wait before trigger the event                                                                                                                                                | 0               |
| **Toast variant** | The color variant of the toast message that will be shown after triggering the event. It is also possible to choose \<None> which disables the toast display.                                            | Neutral         |
| **Toast message** | The message content that appears after the event is successfully triggered                                                                                                                               | Event triggered |

