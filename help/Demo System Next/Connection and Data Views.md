---
title: Connection and Data Views
slug: js6E-c
createdAt: Tue Apr 23 2024 07:18:13 GMT+0000 (Coordinated Universal Time)
updatedAt: Tue Apr 23 2024 07:54:44 GMT+0000 (Coordinated Universal Time)
---

Connection allows us to collect data from multiple sources like website, mobile, marketing campaigns etc. and unify profile and experience events by using common profile identity. To know details about how connection works in CJA [check documentation.](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/overview.html?lang=en)

# Connection

**Name**: [Demo System - Binji+ Connection](https://experience.adobe.com/#/@demosystem4/platform/analytics/#/apps/data-management/connections/dg_f63b57a9-8fe2-45f0-9456-f93b73b40dcd)

**Org**: Adobe Demo System Shared

**Sandbox**: Public Project - Binji



![Binji+ Connectio](../../assets/Tt80coWUGeYpn3w7LdWUX_image.png "Binji+ Connection")

::::tabs
:::tab{title="Experience Event Datasets"}
- Demo System - CJA - Website Dataset
- Demo System - CJA - Dataset for Mobile
- Demo System - CJA - Dataset for AJO Step Events
- Demo System - CJA - Dataset for AJO Message Feedback
- Demo System - CJA - Dataset for AJO Message Tracking
:::

:::tab{title="Look-up Datasets"}
- Demo System - CJA - Dataset for AJO Entity Record
:::

:::tab{title="Profile Dataset"}
- Demo System - CJA - Dataset for CRM Profiles
:::

:::tab{title="Profile Identity (Stitching)"}


- For experience event datasets&#x20;
  `_demosystem4.identification.core.crmId`
- For AJO datasets
  `identityMap (``crmId``)`
- For AJO Entity lookup
  Key: `_experience.customerJourneyManagement.entities.channelDetails.messageID`
  Matching key: `_experience.customerJourneyManagement.messageExecution.messageID`
:::
::::



# Data view

:::hint{type="warning"}
While customising existing projects, please make a copy of "**Data view**" & "**Project**".
:::

**Name**: [Demo System - Binji+ Data view (v1.0)](https://experience.adobe.com/#/@demosystem4/platform/analytics/#/apps/data-management/data-views/edit/dv_66254d065a30005169278c35)

**Session length**: 8 hours

![Binji+ Data view](../../assets/RgNPiy49nrlMFaKY2wG3a_image.png "Binji+ Data view")

::::tabs
:::tab{title="Filters / Segments"}
- Binji+ Live audience
- Music lovers
- Sports enthusiast
- Podcast attendees
:::
::::



