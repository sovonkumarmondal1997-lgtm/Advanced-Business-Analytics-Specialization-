# Buy-Till-You-Die Models: Predicting Long-Term Customer Behavior

Traditional regression models are excellent for predicting what customers will do in the next period. However, they become less effective when businesses need to make predictions far into the future, such as estimating customer lifetime value or determining when a customer will stop purchasing. To address this challenge, customer analytics often uses **probability models**, which focus on the underlying behavioral processes that generate customer actions rather than directly predicting future outcomes. :contentReference[oaicite:0]{index=0}

## Regression vs. Probability Models

Regression models use available customer information to predict future behavior. They work well when forecasting the next period because they rely on observable variables such as purchases, marketing activity, demographics, or customer interactions.

Probability models take a different approach. Instead of focusing only on observed data, they attempt to explain the hidden processes that generate customer behavior. The goal is to understand what is happening beneath the surface and use that understanding to make long-term predictions. :contentReference[oaicite:1]{index=1}

## The Purchase Coin

The model assumes that customer purchasing behavior is probabilistic. Rather than trying to explain every individual decision, customer actions are treated as if they were random outcomes.

Imagine each customer has a personal "purchase coin":

- Heads = Customer makes a purchase.
- Tails = Customer does not make a purchase.

The important idea is that different customers have different coins.

For example:

- One customer may have a 90% chance of purchasing.
- Another may have only a 10% chance of purchasing.

This difference is called **heterogeneity**, meaning customers have different purchasing propensities. The model focuses on estimating these underlying tendencies rather than predicting every individual purchase. :contentReference[oaicite:2]{index=2}

## The Death Coin

Purchase behavior alone is not enough. A customer may stop purchasing permanently.

To represent this, the model introduces a second coin called the **death coin**.

- Heads = Customer remains active.
- Tails = Customer permanently leaves the customer base.

The term "death" does not refer to physical death. Instead, it means the customer becomes inactive and is unlikely to return.

Possible reasons include:

- Switching to competitors.
- Losing interest.
- No longer needing the product.
- Moving away from the market.

Once the death coin lands on tails, the customer is considered permanently inactive. :contentReference[oaicite:3]{index=3}

## Understanding Customer Activity

The model explains why recency is often more important than frequency.

Consider two customers:

### Mary
Purchased recently.

### Sharmila
Purchased frequently in the past but missed the most recent period.

The recent inactivity of Sharmila may indicate that her death coin has already landed on tails, meaning she may have permanently left. Mary's recent activity suggests she is still active and therefore more likely to purchase again.

This reasoning explains why recency is often a stronger predictor of future behavior than frequency alone. :contentReference[oaicite:4]{index=4}

## Heterogeneity Across Customers

Both purchase and death probabilities vary across customers.

Some customers:

- Purchase frequently.
- Remain active for long periods.

Others:

- Purchase rarely.
- Leave quickly.

The model allows these probabilities to differ across individuals rather than assuming all customers behave the same way. This flexibility greatly improves long-term forecasting accuracy. :contentReference[oaicite:5]{index=5}

## Buy-Till-You-Die (BTYD) Model

Combining the purchase coin and death coin creates a **Buy-Till-You-Die (BTYD) Model**.

The process works as follows:

1. Customer starts active.
2. Each period, the death coin is flipped.
3. If the customer remains active, the purchase coin is flipped.
4. The process continues until the death coin indicates permanent inactivity.

This simple probabilistic framework can effectively model:

- Purchases.
- Donations.
- Website visits.
- App usage.
- Insurance claims.
- Subscription activity.
- Many other recurring customer behaviors. :contentReference[oaicite:6]{index=6}

## Why BTYD Models Matter

BTYD models are especially valuable when businesses need to answer long-term questions such as:

- How long will a customer remain active?
- How many future purchases will occur?
- What is the customer's lifetime value?
- Which customers deserve additional investment?

While regression often performs best for short-term predictions, BTYD models are designed specifically for long-term forecasting and customer lifetime value analysis. :contentReference[oaicite:7]{index=7}

## Key Takeaway

Buy-Till-You-Die models explain customer behavior using two hidden processes: a purchase propensity and a dropout propensity. By treating customer actions as probabilistic and allowing customers to differ in both buying and dropout tendencies, these models can generate powerful long-term predictions about retention, purchasing behavior, and customer lifetime value. This makes them one of the most important frameworks for long-term customer analytics.