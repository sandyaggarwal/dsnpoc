---
title: Federated Audience Composition (FAC)
slug: YJV3-federated-audience-c
createdAt: Mon Aug 19 2024 12:06:26 GMT+0000 (Coordinated Universal Time)
updatedAt: Tue Sep 17 2024 11:18:59 GMT+0000 (Coordinated Universal Time)
---

## Product documentations & Availability

Federated Audience Composition (FAC) in Experience Platform enables you to access and create audiences with corresponding high-value attributes from enterprise data warehouses, which enrich and supplement the real-time customer profile and audiences in Experience Platform for improved segmentation, targeting, activation, and delivery of impactful customer experiences. Using Federated Audience Composition, a virtual database is created by linking remote databases through metadata. This approach simplifies access, reduces duplication, and enhances end-user experience.

[Federated Audience Composition (FAC) Overview](https://experienceleague.adobe.com/en/docs/federated-audience-composition/using/home)

[**Federated Audience Composition (FAC) Tutorial**](https://experienceleague.adobe.com/en/docs/platform-learn/tutorials/audiences/overview-of-federated-audience-composition)

[Getting started with audience composition](https://experienceleague.adobe.com/en/docs/federated-audience-composition/using/compositions/gs-compositions)

[Federated Audience Composition FAQ](https://experienceleague.adobe.com/en/docs/federated-audience-composition/using/start/faq)

:::hint{type="info"}
Federated Audience Composition feature is enabled at sandbox level.

Enabling this feature creates product profile, of the format `ACP_FAC - <sandbox> - admin`, in Adobe Experience Platform product. Users need to be added to this product profile, to be able to access feature.
:::

## Availability

Shared demo instances with Federated Audience Composition (FAC) enabled:

- **Adobe Demo System Shared** (`demosystem4`)
  - Public project - Luma
    - **Available**: Database connection, Schemas, Data model, Composition
  - Public project - SecurFinancial
    - **Available**: Database connection, Schemas, Data model, Composition
  - Prod
    - **Available**: Database connection, Schemas, Data model
- **Adobe Demo System Individual** (`demosystem5`)
  - Prod
    - **Available**: Database connection, Schemas, Data model
- **Demo EMEA** ( `demoemea` )
  - Luma EMEA
    - **Available**: Database connection, Schemas, Data model
  - Securfinancial EMEA
    - **Available**: Database connection, Schemas, Data model

:::hint{type="danger"}
DO NOT MODIFY EXISTING ASSETS.
:::

## Accessibility

Request administrator of the instance to add users to `ACP_FAC - <sandbox> - admin` product profile / related user group.

![](../../assets/y3GPHctfS54SEbskGzc6U_screenshot-2024-08-19-at-80206-pm.png)

- **Models**
  - Allows you to explore Schemas and Data models (relationships)
- **Audit trail**
  - Allows you to see the change history in federated database connection management
- **Federated databases**
  - Allows you to browse through different databases available to connect/use

***

**Audience Composition**

![](../../assets/j_hyweeLSR8T1IS4OtMHY_screenshot-2024-08-19-at-81118-pm.png)

**Browse resultant audiences**

![](../../assets/AvjQjGs0T0UnbFslNeDRx_screenshot-2024-08-19-at-81220-pm.png)

:::hint{type="warning"}
If you already have access to FAC in a sandbox; and you notice `Error 403: Access not allowed`, please try connecting through VPN
:::



## Retail scenario

### Database connection

**Name**: Demo\_System\_Next\_\_Retail\_Federated\_Source

**Type**: Snowflake

**Database**: CUSDEVDB1

### Entities & Relationships

![Luma Entities Relationship](../../assets/3No08EyrgaKWmPM4jyG35_fac-retail-erd.png "Luma Entities ")

### Compositions

**Use-case 1: Loyalist and Women Category**

*Customers whose category affinity is equal to women, and they are signed up for the loyalty program.*

**Create audience**:

- "Favourite category" is "Women"
- "Loyalty status" greater than 1
- Having average order value greater than $50
- Agreed for marketing consent

**Highlight**: Enrichment

**Scheduled**: No

**Result audience name**: Luma - Loyalist and Women Category

**Identity**: Email

![](../../assets/QbK10pC79D9nhH7uVYOeZ_fac-loyalist-and-women-category.png)

**Use-case 2: Luma - Birthday Month offers**

*Create audience of customers who have a birthday this month, if they have an active order, target them for a birthday offer that references their order status. However, if they do not have an active order, just target them with a birthday offer.*

**Create audience**:

- Birthdate falls in current month
- Based on "Order" exists for the target audience split into two categories of audience.

**Highlight**: Conditional split, Enrichment

**Scheduled**: No

**Result audience name**: Luma - Birthday this month offer - active order, Luma - Birthday this month offer

**Identity**: Email

![](../../assets/tmKJsD662oy_Jv8tR03VI_fac-luma-birthday-month-offer.png)



**Use-case 3: Luma - Customer Avg. Order > $100**

*Prior Order History is greater or equal to $100 and has consented to marketing communications. Additionally, with enrichment, we can also couple together this output with, “does a Wishlist exist?” for this specific user – this could warrant retargeting or offers being sent to that user when an item / product on their wish list changes price or stock levels.*

**Create audience**:

- Total order value greater than $100
- Age greater than 20
- Agreed for marketing consent
- Based on linked "Wishlist" items split into two categories of audience.

**Highlight**: Conditional split, Enrichment

**Scheduled**: No

**Result audience name**: Luma - Prime customer wishlist, Luma - Prime customer recommendations

**Identity**: Email

![](../../assets/3yRdiYU4XICMt88nAcHGj_fac-luma-avg-order-val.png)

***

## FSI Scenario

### Database connection

**Name**: Demo\_System\_Next\_\_SecurFinancia\_Federated\_Source

**Type**: Snowflake

**Database**: CUSDEVDB2

### Entities & Relationships

![](../../assets/nII7qLSw_LlU-Kb-ZKA5X_fac-fsi-erd.png)

### Compositions

**Use-case 1: SecurFinancial - PREMIUM Card Upgrade Prospects**

*Customers segment for premium card feature promotion.*

**Create audience**:

- "Credit score" greater than 67
- "Card upgrade prediction" greater than 80

**Scheduled**: Yes, Once on weekdays

**Result audience name**: SecurFinancial - Eligible for upgrade

**Identity**: Email

![](../../assets/x7P92lvu_GjXHj0qpFB8S_fac-fsi-premium-card.png)

**Use-case 2: SecurFinancial - Co-branded eligibility**

*Pre- approved for a co-branded credit card using the event types of either transaction, payment, or information*

**Create audience**:

- "Promotion type" equals "Cobranded Credit Card"
- Customer should have "Transaction" / "Payments" / "Information" enquiries
- Based on recent transaction flag, split the audience in two categories

**Scheduled**: Yes, Once on weekdays

**Result audience name**: Pre-approved for cobranded credit card, Cobranded credit card eligible

**Identity**: Email

![](../../assets/yuS0RoUFLm9xaXMiIVYIF_fac-fsi-cobranded-cc.png)

**Use-case 3: SecurFinancial - High valued customers**

*Segment audience based on customer engagement and categorise them for Home loan and various card promotions. If customer has credit card, promote home loan; otherwise promote credit cards.*

**Create audience**:

- Target customers belonging to segments "Silver" and "Gold"
- Having scores for car loan / home loan / personal loan greater than 60
- Online users (i.e. events source in mobile app or online)

**Scheduled**: No

**Result audience name**: SecurFinancial - Home Loan Prospects, SecurFinancial - PREMIUM CC Prospects, SecurFinancial - GOLD CC Prospects

**Identity**: Email

![](../../assets/X1YLl9UtpMoyctdhnVFrN_fac-fsi-high-valued-customer.png)

***

## Destination

While activating audience and enriched attributes, you could leverage existing "**Federated Audience Composition**" (Type: Adobe Applications) destination for *Demo System Next*, which is a **Snowflake** database; or, you may choose to create a new destination.



![Use the new FAC destination icon, with Adobe logo.](../../assets/Z2THjxuqOROdP4ZIbQwyc_image.png "Use the new FAC destination icon, with Adobe logo.")

