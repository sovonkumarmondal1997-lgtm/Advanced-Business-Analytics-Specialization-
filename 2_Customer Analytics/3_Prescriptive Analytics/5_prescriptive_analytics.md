# Prescriptive Analytics: Asking the Right Question, Competition, and Advertising Attribution

A critical lesson in prescriptive analytics is that the quality of a recommendation depends on the quality of the question being asked. Even when using the same data, changing the objective, assumptions, or model can produce completely different recommendations. Therefore, before choosing an action, businesses must carefully understand what they are trying to maximize and how consumers and competitors behave in the market. :contentReference[oaicite:0]{index=0}

## Why Asking the Right Question Matters

Throughout previous examples, the same demand data produced different recommendations depending on the objective.

### Maximize Quantity Sold

Recommendation:

- Charge a very low price.

### Maximize Revenue

Recommendation:

- Charge a higher price.

### Maximize Profit

Recommendation:

- Charge an even higher price after accounting for costs.

The data remained unchanged, but the recommended action changed because the business objective changed. This demonstrates why selecting the correct objective is one of the most important steps in prescriptive analytics. :contentReference[oaicite:1]{index=1}

## Strategic Interaction and Competition

Earlier pricing models assumed that competitors would not react to a company's decisions.

In reality, competitors often respond strategically.

For example:

1. Company A lowers its price.
2. Company B responds by lowering its price.
3. Company A lowers its price again.
4. Company B responds again.

This process can continue repeatedly and create a **price war**.

### Price War

A price war occurs when competing firms continuously reduce prices in response to one another.

Consequences include:

- Lower profit margins.
- Reduced profitability for all firms.
- Potential profits approaching zero.

This shows that pricing decisions cannot be analyzed in isolation when competitors are present. :contentReference[oaicite:2]{index=2}

## Strategic Interaction

Strategic interaction occurs when:

- One firm's decision affects another firm's decision.
- Competitors react to each other's actions.
- Outcomes depend on the choices of multiple participants.

In such situations, optimal decisions depend not only on customer behavior but also on competitor behavior. :contentReference[oaicite:3]{index=3}

## Role of Game Theory

The field that studies strategic interaction is called:

:contentReference[oaicite:4]{index=4}

Game theory helps analyze situations where:

- Multiple firms interact.
- Decisions are interdependent.
- Competitors respond strategically.

It extends prescriptive analytics beyond simple optimization by considering the actions and reactions of other market participants. :contentReference[oaicite:5]{index=5}

## Online Advertising Decisions

Another important prescriptive analytics problem involves online advertising.

Companies must decide:

- Which consumers should see an advertisement?
- How often should an advertisement be shown?
- On which websites should the advertisement appear?

Since advertising budgets are limited, firms need to allocate ads efficiently. :contentReference[oaicite:6]{index=6}

## Multi-Channel Advertising

Consumers often visit multiple websites.

Examples:

- News websites.
- E-commerce sites.
- Search engines.
- Social platforms.

Advertisers may choose to display the same advertisement repeatedly across multiple websites.

This strategy is commonly used in retargeting campaigns, where advertisements follow users after they have viewed a product or visited a website. :contentReference[oaicite:7]{index=7}

## Attribution

A major challenge in advertising is determining whether an advertisement actually influenced a customer's behavior.

This problem is called **attribution**.

Attribution attempts to answer:

- Which advertisement caused the purchase?
- Which marketing channel influenced the customer?
- How much credit should each advertisement receive?

These questions are difficult because customers often encounter many advertisements before making a purchase decision. :contentReference[oaicite:8]{index=8}

## Click-Through Rate (CTR)

One commonly used advertising metric is the Click-Through Rate (CTR).

CTR measures the percentage of users who click on an advertisement.

The formula is:

:contentReference[oaicite:9]{index=9}

Where:

- Clicks = Number of ad clicks.
- Ad Impressions = Number of times the ad was shown.

CTR is often used as an indicator of advertising effectiveness. :contentReference[oaicite:10]{index=10}

## Example: Number of Ads vs. Click Rate

Suppose analysts examine data showing:

- Some consumers see no advertisements.
- Some consumers see one advertisement.
- Others see advertisements on multiple websites.

The observed pattern shows:

- More advertisements → Higher click-through rates.

At first glance, this suggests that repeatedly showing ads makes them more effective and increases the likelihood that consumers will click. :contentReference[oaicite:11]{index=11}

## The Important Question

However, prescriptive analytics requires asking:

> Does the observed relationship truly represent causation?

The key question is:

- Are more advertisements causing more clicks?
- Or are certain consumers naturally more likely to click advertisements regardless of how many ads they see?

This distinction is critical because incorrect assumptions can lead to poor recommendations and wasted advertising budgets. :contentReference[oaicite:12]{index=12}

## Key Takeaway

Prescriptive analytics depends on asking the correct business question and selecting the appropriate model. The same data can produce different recommendations depending on the objective being optimized. When competitors exist, strategic interactions and price wars must be considered, often requiring game theory. In digital advertising, attribution and click-through rate analysis help evaluate marketing effectiveness, but analysts must be careful not to confuse correlation with causation. Successful prescriptive analytics therefore requires not only data and models but also a deep understanding of market behavior and decision-making dynamics. :contentReference[oaicite:13]{index=13}