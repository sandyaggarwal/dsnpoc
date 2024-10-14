---
title: Environment Admin
slug: pHw7-mana
createdAt: Mon Nov 27 2023 18:35:55 GMT+0000 (Coordinated Universal Time)
updatedAt: Wed Nov 29 2023 12:57:59 GMT+0000 (Coordinated Universal Time)
---

In order to access IMS Organizations and Experience Platform sandboxes, users need to be granted appropriate access within Demo System Next, separate from actual provisioning inside Adobe Experience Cloud. This means, that each user needs to be assigned to IMS org and sandbox in order to use it in eg. Quick Setup.

There are two primary self-service tools:&#x20;

1. [IMS Org Admin](<../Demo System Next/IMS Org Admin.md>) - allowing admins to add or update IMS Orgs and integration details
2. Environment Admin - allowing to assign users to orgs and sandboxes to users.

## Environment Admin

<https://dsn.adobe.com/tools/environment-admin>

![](../../assets/83IoGQ5Z43CLy6fcO25V4_image.png)

This view allows you to assign others to orgs as both users and admins, and specify which sandboxes should be visible for them in DSN. This affects which environments (org/sandbox) can be selected by them in Quick Setup, or viewed on environment list.

Removing user (or self) from an org in this view unassigns them from org altogether, so be careful not to remove yourself from an administered org by accident.

