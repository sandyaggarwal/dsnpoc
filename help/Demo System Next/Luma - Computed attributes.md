---
title: Luma - Computed attributes
slug: 2arf-com
createdAt: Wed Oct 25 2023 19:13:02 GMT+0000 (Coordinated Universal Time)
updatedAt: Fri Oct 27 2023 13:10:59 GMT+0000 (Coordinated Universal Time)
---

To learn more about computed attributes please read this article: [Computed Attributes](<../Demo System Next/Computed Attributes.md>)

# Exclusive Reward Program

Luma aims to incentivize customer spending by introducing an Exclusive Reward Program. Customers who spend a specific amount within a short time period are rewarded with exclusive perks.
Utilizing the Adobe Experience Platform, Luma computes real-time purchase totals to identify eligible customers. Once a customer reaches the spending threshold, a personalized reward notification is sent, offering an exclusive discount on their next purchase. This not only drives sales but also enhances customer loyalty and engagement by recognizing and rewarding their spending behavior, making them feel valued and encouraged to continue shopping with Luma.

Below you can find the predefined Computed Attributes you can also use in your talk track.

### Computed attributies available for Luma brand:

### Sales and Purchasing Metrics

| Name                       | Description                                       | Aggregate Function | Lookback period |
| -------------------------- | ------------------------------------------------- | ------------------ | --------------- |
| TotalPurchasesAmount       | Sum of all purchases made by a customer           | SUM                | 6 months        |
| TotalPurchases             | Count of all purchases made by a customer         | COUNT              | 6 months        |
| WeeklyTotalPurchasesAmount | Sum of all purchases made by a customer last week | SUM                | 7 days          |
| MaxPurchaseValue           | Maximum purchase value in the last 6 months       | MAX                | 6 months        |
| MinPurchaseValue           | Minimum purchase value in the last 6 months       | MIN                | 6 months        |
| TotalDiscounts             | Total discounts offered to a customer             | COUNT              | 6 months        |
| RewardsPoints              | Total reward points accumulated by a customer     | SUM                | 6 months        |
| MostRecentProductPurchased | The most recent purchase made by a customer       | MOST\_RECENT       | 24 hours        |
| MostRecentDiscount         | The most recent discount availed by a customer    | MOST\_RECENT       | 7 days          |

### Customer Engagement Metrics

| Name                      | Description                                    | Aggregate Function | Lookback period |
| ------------------------- | ---------------------------------------------- | ------------------ | --------------- |
| EmailSentLastMonth        | Count of all emails sent to a customer         | COUNT              | 1 month         |
| emailLinkClickedLastMonth | Count of all email links clicked by a customer | COUNT              | 1 month         |
| RecentSubscription        | Most recent List Subscription                  | MOST\_RECENT       | 7 days          |

### Customer Behaviour Metrics

| Name                      | Description                                 | Aggregate Function | Lookback period |
| ------------------------- | ------------------------------------------- | ------------------ | --------------- |
| LastVisitedStore          | The most recent store visited by a customer | MOST\_RECENT       | 7 days          |
| TotalStoreVisitsLastMonth | Count of all store visits last month        | COUNT              | 1 month         |
| PurchaseFrequency         | Number of purchases made in the last month  | COUNT              | 1 month         |
| LastProductViewed         | The last product viewed by a customer       | MOST\_RECENT       | 24 hours        |
| ProductViewsLastMonth     | Number of products viewed in the last month | COUNT              | 1 month         |
| MostRecentPartnerID       | Most recent Partner ID from web visitors    | MOST\_RECENT       | 7 days          |

