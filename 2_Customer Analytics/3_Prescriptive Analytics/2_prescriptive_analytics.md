# Prescriptive Analytics: Revenue Maximization and Optimization

Prescriptive analytics can generate very different recommendations from the same data depending on the business objective being optimized. This highlights a key principle of prescriptive analytics: the best decision depends on the goal. Using the same demand curve and regression model, a company may choose one action if it wants to maximize sales volume and a completely different action if it wants to maximize revenue. :contentReference[oaicite:0]{index=0}

## The Power of Prescriptive Analytics

Unlike descriptive and predictive analytics, prescriptive analytics focuses on recommending actions.

The process involves three components:

### Objective (Goal)
What the company wants to optimize.

### Action (Decision Variable)
What the company can control.

### Model
How actions influence outcomes.

Different objectives can produce completely different recommendations even when using the same underlying data. :contentReference[oaicite:1]{index=1}

## Revenue Maximization Problem

In this example, the objective changes from maximizing quantity sold to maximizing revenue.

### Objective

Maximize revenue.

### Action

Set or change the product price.

### Model

Use the demand curve (or regression equation) that describes how demand changes when price changes. :contentReference[oaicite:2]{index=2}

## How Revenue Is Calculated

Revenue is determined by multiplying price and quantity sold.

:contentReference[oaicite:3]{index=3}

This creates an important trade-off because changing price affects both parts of the equation simultaneously. :contentReference[oaicite:4]{index=4}

## Understanding the Trade-Off

### When Price Decreases

- More units are sold.
- Revenue earned per unit decreases.

### When Price Increases

- Fewer units are sold.
- Revenue earned per unit increases.

Because one factor rises while the other falls, it is impossible to determine the best price simply by intuition. A formal model is required. :contentReference[oaicite:5]{index=5}

## What Is a Trade-Off?

A trade-off occurs when a decision improves one aspect of performance while potentially harming another.

In pricing:

- Lower prices increase demand.
- Higher prices increase revenue per unit.

The optimal decision depends on balancing these competing effects. Prescriptive analytics helps identify that balance. :contentReference[oaicite:6]{index=6}

## Finding the Revenue-Maximizing Price

The process involves:

1. Selecting a range of possible prices.
2. Using the demand model to estimate quantity sold at each price.
3. Calculating revenue for each price.
4. Comparing the results.
5. Choosing the price that generates the highest revenue.

For example:

- Price = $3.00
- Demand = 7.43 units

Revenue:

:contentReference[oaicite:7]{index=7}

Repeating this calculation for many prices creates a revenue table and revenue curve. :contentReference[oaicite:8]{index=8}

## Revenue Curve

When revenue is plotted against price:

- Revenue initially increases as price rises.
- Revenue reaches a maximum point.
- Revenue eventually decreases as price becomes too high and demand falls significantly.

The highest point on the curve represents the optimal price for maximizing revenue. :contentReference[oaicite:9]{index=9}

## Optimal Price

Using the demand model from the example:

- The revenue-maximizing price is approximately **$5.50**.

This price generates the highest total revenue even though it does not generate the highest sales volume. :contentReference[oaicite:10]{index=10}

## Same Data, Different Recommendations

The most important lesson is that identical data can produce different recommendations depending on the objective.

### Goal: Maximize Quantity Sold

Recommendation:

- Set price = $0
- Give the product away for free.

Reason:

- Free products generate maximum demand.

### Goal: Maximize Revenue

Recommendation:

- Set price ≈ $5.50

Reason:

- This price balances demand and price to maximize total revenue.

The difference arises entirely from changing the objective, not the data. :contentReference[oaicite:11]{index=11}

## General Prescriptive Analytics Framework

Every prescriptive analytics problem follows the same structure:

### Objective
What should be optimized?

Examples:

- Revenue
- Profit
- Market share
- Customer retention
- Costs

### Actions
What decisions can be controlled?

Examples:

- Pricing
- Promotions
- Advertising
- Product availability

### Model
How do actions affect outcomes?

Examples:

- Demand models
- Regression models
- Customer response models

Optimization then identifies the action that best achieves the objective. :contentReference[oaicite:12]{index=12}

## Key Takeaway

Prescriptive analytics uses objectives, actions, and models to recommend optimal decisions. The same customer data can lead to very different recommendations depending on the business goal. In the pricing example, maximizing quantity suggests giving the product away for free, while maximizing revenue suggests charging approximately $5.50. This demonstrates that successful decision-making depends not only on understanding data but also on clearly defining what the organization wants to achieve. :contentReference[oaicite:13]{index=13}