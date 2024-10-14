---
title: Activity Timeline
slug: kCGa-activity-timeline
createdAt: Thu Oct 26 2023 11:50:56 GMT+0000 (Coordinated Universal Time)
updatedAt: Wed Feb 28 2024 16:43:33 GMT+0000 (Coordinated Universal Time)
---

**Activity Timeline **displays experience events as cards in a timeline. Events can be filtered by channels and types. Each event can be clicked on to display a sidebar with more details.

![](../../assets/UVWcKBqUS66kqDYpgKu6N_image.png)

## Displaying event details in the sidebar

Clicking on an event card opens the sidebar view of that event. The purpose of the sidebar view while browsing the events is to display more specific details about the events. Each of the event types can be configured to display customized details in the sidebar view, by modifying the custom information labels and values, including what the source of the information to put into the sidebar is.

![](../../assets/FxqV2NB1bV5Wufdj8MQfJ_image.png)

## Module configuration

### General settings

| **Property**    | **Description**                                                                                                                                                                    | **Default**                                                         |
| --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| **Hide title**  | Indicates whether the module title above the module content should be hidden or not                                                                                                | false                                                               |
| **Title**       | The name of the module, displayed above the module content                                                                                                                         | Customer Touchpoints                                                |
| **Description** | The description of the module, displayed as a tooltip after clicking on the info icon next to the module's title                                                                   | activity timeline                                                   |
| **Channel**     | List of names of the channels that the events should be filtered by. The filtering of these channels can be applied after clicking on the filter button next to the module's title | 'web', 'mobile', 'call-center', 'crm', 'cx', 'ar', 'chatbot', 'iot' |

### Event types

| **Property**              | **Description**                                                                                                                                                                                                                                                                       |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **ID**                    | The identifier of the event type                                                                                                                                                                                                                                                      |
| **Name**                  | The name of the event type, used as an event title in case the title is not specified.                                                                                                                                                                                                |
| **Title**                 | The title of the event of this type. It can either be a path in an event object, a simple string or a combination of both, e.g. "Simple string ${path}"                                                                                                                               |
| **Image path**            | Path in the event JSON object that points to the image of the event. If empty or not found, thumbnail will be used as fallback.                                                                                                                                                       |
| **Thumbnail**             | An image of the event. Icon is used as fallback                                                                                                                                                                                                                                       |
| **Icon**                  | An icon chosen to represent the event type in the timeline                                                                                                                                                                                                                            |
| **Custom sidebar fields** | Allow you to customize what kind of information of the event goes into the sidebar view. A JSON representing an object or an array of objects, each of which contains two properties: label and value, which specify the additional details to be presented in an event sidebar view. |

## Custom sidebar fields

You can set custom sidebar fields as part of the module configuration for each event type. By providing a JSON object or an array of objects you can specify exactly what extra event information should be displayed within the sidebar.

An object should look as follows:

```json
{
  "label": "<STATIC OR DYNAMIC VALUE>",
  "value": "<STATIC OR DYNAMIC VALUE>"
}
```

You can use static or dynamic values to be displayed in the sidebar. The static values are simply strings. The dynamic values are path selectors for an event information from AEP. You can specify it either by simply inputting the string or enclosing it in the `${}` brackets.

:::hint{type="info"}
Dynamic selectors that fail to resolve will fallback to themselves. If you want to avoid that and have an empty value displayed instead, ensure that the selector is enclosed in `${}` bracket.
:::

### Examples

```json
{
  "label": "A static label",
  "value": "A static value"
}
```

```json
{
  "label": "Time of the event",
  "value": "entity.timestamp" // will resolve to "entity.timestamp" if not found
}
```

```json
{
  "label": "Time of the event",
  "value": "${entity.timestamp}" // will resolve to "--" if not found
}
```

```json
{
  "label": "Time of the event",
  "value": "The date is: ${formatDate:entity.timestamp}" // will resolve to "--" if not found
}
```



