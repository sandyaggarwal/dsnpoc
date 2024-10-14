---
title: Event Trigger
slug: j4d71Rd14r3YYukeJd2J0
createdAt: Thu Oct 26 2023 11:51:05 GMT+0000 (Coordinated Universal Time)
updatedAt: Mon Jan 08 2024 13:16:48 GMT+0000 (Coordinated Universal Time)
---

The **Event Trigger **module displays configured event details with a button to trigger the event. In contrary to the [Button](<../Demo System Next/Button.md>) module which sends events by triggering Data Collection Rules, Event Trigger sends the events directly to the EDGE service which allows rapid dispatch of the event and recording it in the AEP.

![](../../assets/chCzPzJz2AVzHMQBF7HAk_untitled-4.png)

## Configuration details

As the EDGE service requires the ID of the **datastream** which the events are sent to, you must specify such datastream in the module configuration before you will be able to send events. The datastream created together with your project when going through the Quick Setup process will be chosen by default. You can choose another one if you wish. If you haven't configured your integrations or for any other reason it was not possible to fetch your datastreams, you will be required to provide the datastream ID of your choosing manually.

Further on, you can choose one of two configuration types for your Event Trigger module:

- **Simplified**

  You can specify the name of the event that will be included in the basic payload sent to the EDGE service.
- **Advanced**

  You can provide your own additional data in the payload that will be sent to the EDGE service. This payload has to match the template for the event dispatch to become effective.

Whichever option you choose, ultimately the payload will be populated with the *identity data* of the currently browsed profile, to match the schema of the datasets.

### Advanced payload template

```json
{
  "event": {
    "xdm": {
      "eventType": "",
      "$tenantId": {
        // this part is additionally populated by the identity data
        "interactionDetails": { "core": { "channel": "cx" } },
        "brandName": "$brandName"
      }
      // this part is additionally populated by an ID, timestamp and an
      // identity map
    },
    "data": {}
  }
}
```

## Module configuration

### General settings

| **Property**    | **Description**                                                 | **Default**                           |
| --------------- | --------------------------------------------------------------- | ------------------------------------- |
| **Title**       | The name of the module, displayed as part of the module content | Event Trigger                         |
| **Description** | The description of the module, displayed under the title        | Click the button to trigger an event. |

### Configuration settings

| **Property**           | **Description**                                                                                      | **Default**                                                                                                           |
| ---------------------- | ---------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| **Datastream**         | A datastream the events will be sent to                                                              | Chosen based on the Data Collection property name similarity or blank if not possible to fetch datastreams by default |
| **Configuration type** | Simplified (just event name) or advanced (payload template)                                          | Simplified                                                                                                            |
| **Event name**         | The name of the event to be dispatched with the simplified configuration type                        | --                                                                                                                    |
| **Payload**            | The payload dispatched with the advanced configuration type                                          | *Payload template*                                                                                                    |
| **AJO Test Mode**      | Adds a `joTestModeEvent_` prefix to the event ID to allow the application to work with AJO Test Mode | false                                                                                                                 |

### Appearance settings

| **Property**           | **Description**                                                                                                                     | **Default**   |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ------------- |
| **Button label**       | The label of the button triggering the event                                                                                        | Trigger event |
| **Image**              | An image displayed as a thumbnail or a cover of the Event Trigger                                                                   | --            |
| **Image Variant**      | Indicates whether the image should be a thumbnail next to the Event Trigger content or a cover serving as background of the content | Thumbnail     |
| **Text color**         | Adjust the color of the text content of the module. Useful when using the background image variant                                  | --            |
| **Direction**          | Direction of the text content and the button inside the module                                                                      | Vertical      |
| **Alignment**          | The horizontal alignment of the text content of the module                                                                          | Left          |
| **Vertical alignment** | The vertical alignment of the text content of the module                                                                            | Middle        |

