---
title: Update Profile
slug: fyPAPZJGs-o0p-JgdIRiY
createdAt: Thu Oct 26 2023 11:51:05 GMT+0000 (Coordinated Universal Time)
updatedAt: Tue Nov 28 2023 12:54:22 GMT+0000 (Coordinated Universal Time)
---

The **Update Profile **module displays a form which let you update Real Time Customer Profile attributes.

![](../../assets/hAcqEL26iRe9TDRtfri-g_untitled-6.png)

## Configuration details

The module works by sending partial row updates to Real-Time Customer Profile using streaming upserts in Data Prep. For proper update process it is therefore necessary to provide dataset ID which the profile updates will be done in.

By default, the module will use *Profile Dataset for Customer Experience App*, if available. You can also use a custom dataset ID.

:::hint{type="warning"}
Make sure that the dataset which ID you provide is configure to handle upserts, as this will **ensure** the proper partial row update. Otherwise updating nested values may result in overwriting and loss of profile attributes data.
:::

## Module configuration

### General settings

| **Property**          | **Description**                                                        | **Default**                                      |
| --------------------- | ---------------------------------------------------------------------- | ------------------------------------------------ |
| **Title**             | The name of the module, displayed as part of the module content        | Update Profile                                   |
| **Description**       | The description of the module, displayed under the title               | Edit the fields to update the profile attributes |
| **Dataset type**      | Indicates whether the default dataset should be chosen or a custom one | Default                                          |
| **Default dataset**   | A purely informative element, displays details of the default dataset  | --                                               |
| **Custom dataset ID** | The ID of the custom dataset chosen to update the profiles at          | --                                               |

### Attributes

![](../../assets/dIuFDebL8XFg4Y7bgk_IB_untitled-7.png)

You can specify which attributes are configurable by the module. For each attribute you can choose a label and a type of the input, add a path to the property that is to be updated and specify additional options, if available for the input type.

Some attributes (like identity values) will not be updated as they are needed for identifying a profile to update by the partial row update.

| **Property** | **Description**                                                                            |
| ------------ | ------------------------------------------------------------------------------------------ |
| **Label**    | The label of the input                                                                     |
| **Name**     | The path to the property of the profile to be updated                                      |
| **Type**     | Input type. Could be one of: *Text*, *Number*, *Checkbox*, *Calendar*, *Dropdown*          |
| **Options**  | Additional options to be provided to the input type (for example options for the dropdown) |

