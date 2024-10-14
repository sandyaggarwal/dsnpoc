---
title: CJA B2B Data Details & References
slug: Fjut-c
createdAt: Wed Sep 06 2023 09:12:33 GMT+0000 (Coordinated Universal Time)
updatedAt: Fri Dec 01 2023 04:58:41 GMT+0000 (Coordinated Universal Time)
---

This page contains technical details & FAQs about the B2B CJA demo data.

## Overview

- **Organization**: [Adobe Demo System Shared](https://experience.adobe.com/#/@demosystem4/platform/analytics/#/workspace)
- **Public Project Dashboard**: [Bodea - CJA for B2B](https://experience.adobe.com/#/@demosystem4/platform/analytics/#/workspace/edit/651c7564079ce65bda98002f)
- **Connection Name**: CID - B2B Data
- **Sandbox for Datasets**: [Public Project - Bodea](https://experience.adobe.com/#/@demosystem4/sname\:public-bodea/platform/home)

## Dataset Details

:::hint{type="warning"}
The B2B Opportunity Dataset includes some items that are not out-of-the-box.  Attribution cannot be done at an opportunity level in CJA because CJA is person-based (not account-based).  It is possible to make this happen with a highly custom build, but this should not be presented to a customer without consultation as to the limits and extra steps they would need to take to make it work.  Please reach out to [Kristin Ward](mailto\:krward@adobe.com) by Slack or email with questions.
:::

**Experience Event Datasets**:

- CID-Demo System - B2B Activity Dataset

**Lookup Datasets: **

- CID-Demo System - B2B Campaign Member Dataset
- CID-Demo System - B2B Account Dataset
- CID-Demo System - B2B Opportunity Dataset
- CID-Demo System - B2B Campaign Dataset

**Profile Dataset:**

- CID-Demo System - B2B Person Dataset

![](../../assets/SeuJfAxB8tH8h2RKKZ7--_image.png)

## About Connections & Data Views

**Connections and Data Views**

Connections and data views are the basic building blocks for CJA, that allow to unifying profile/events and interpretation of attribute values, to better understand the customer journey.

**Connection for B2B Project**

The connection allows us to collect data from multiple sources like websites, mobile web, etc., and unify profile and experience events by using a common profile identity. To learn more about how the connection works in CJA [see the documentation.](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/overview.html?lang=en)

**Data View for B2B**

A data view is a container specific to Customer Journey Analytics that lets you determine how to interpret data from a connection. It specifies all dimensions and metrics available in the Analysis Workspace and which columns those dimensions and metrics obtain their data from. Data views are defined in preparation for reporting in the Analysis Workspace. To learn more about Data Views in CJA [see the documentation](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/data-views.html?lang=en)*.*

## FAQs & Troubleshooting

**Unable to see the project in the list of reports?**

Please contact us using the Slack discussion channel, [#demo-system-next](https://sv-core-tech.slack.com/archives/CPCRVPLDQ)**,** and we will add you to the user group.

**Unable to view connection and data view tabs?**

You need to have additional access privileges (refer [doc](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-admin/cja-access-control.html?lang=en#product-admin-role)). Please contact us using the Slack discussion channel, [#demo-system-next]()**,** and we will add you to the user group.

