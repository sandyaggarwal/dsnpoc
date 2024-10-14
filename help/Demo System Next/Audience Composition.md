---
title: Audience Composition
slug: JQqE-aud
createdAt: Mon Sep 04 2023 15:18:53 GMT+0000 (Coordinated Universal Time)
updatedAt: Mon Oct 02 2023 11:50:08 GMT+0000 (Coordinated Universal Time)
---

## What is Audience composition?

Audience composition allows you to create **composition workflows**, where you can combine existing Adobe Experience Platform audiences into a visual canvas and leverage various activities (split, exclude…) to create new audiences.

Once done, the **resulting audiences** are saved and backed into the Adobe Experience Platform along with existing audiences and can be **leveraged in campaigns** to target customers. [Learn how to work with campaigns](https://experienceleague.adobe.com/docs/journey-optimizer/using/campaigns/get-started-with-campaigns.html?lang=en)

![](https://experienceleague.adobe.com/docs/journey-optimizer/assets/audiences-process.png?lang=en)

🔗 [Audience Composition documentation](https://experienceleague.adobe.com/docs/journey-optimizer/using/audiences-profiles-identities/audiences/audience-orchestration/get-started-audience-orchestration.html?lang=en)



## Audience Composition Use cases

### Promote Luma+ loyalty program

Luma's newly launched loyalty program, Luma+, aims to reward our most devoted customers, incentivize repeat purchases, and create a community of brand advocates. This email campaign seeks to introduce and promote the Luma+ loyalty program to our customer base, driving enrollments and enhancing overall customer lifetime value.

**Audience Composition Canvas**

![Audience composition canvas](../../assets/dGpuqFcJGBT7icoqWovJH_cleanshot-2023-09-04-at-174000.png "Audience composition")

Composition activities overview:

1. We can use the **Audience activity **to select our initial targeted audience
2. It is easy to exclude dissatisfied customers with the **Exclude activity**
3. The **Enrich activity **includes the recommended customer's next best offer using an enrichment dataset and a join key
4. **Rank activity **helps us to reorder the customer audience by customers having the highest Lifetime value so far
5. We can create a new audience resulting from this composition using the **Save activity**



View [**Luma - Promote Luma+ Loyalty Program**](https://experience.adobe.com/#/@demosystem4/sname\:public-luma/journey-optimizer/audience/compose/64de20a6f041d279006e2e95) composition.



### Yoga Summer Sale

The Marketing Manager at Luma uses customer data to identify preferred communication channels and creates distinct segments to optimize customer engagement and conversion rates before creating a new Yoga Summer Sale campaign.



**Audience Composition Canvas**

![](../../assets/QpCDZnm0Ux2YWdvlRx9tF_cleanshot-2023-10-02-at-134817.png)

View [Luma - Yoga Summer Sale](https://experience.adobe.com/#/@demosystem4/sname\:public-luma/platform/audience/compose/651a6384ea6dae09a66cf41f) audience composition.
