# Prescriptive Analytics: Causality, Advertising Attribution, and the Limits of Descriptive Data

One of the biggest challenges in prescriptive analytics is distinguishing between **correlation** and **causation**. A pattern observed in descriptive data may appear to suggest that a particular action causes a result, but the relationship may actually be driven by other factors. If businesses incorrectly assume causation from observational data, they may make poor decisions and waste resources. Prescriptive analytics therefore requires careful testing and validation before turning observations into actions. :contentReference[oaicite:0]{index=0}

## The Advertising Example

The lecture examines an online advertising campaign.

### X-Axis

Number of websites showing advertisements to a consumer.

### Y-Axis

Click-Through Rate (CTR), which measures the probability that a consumer clicks on an advertisement.

The initial data appears to show:

- More ad exposures → Higher click-through rates.

At first glance, this suggests that showing consumers more advertisements causes them to click more often. :contentReference[oaicite:1]{index=1}

## The Important Question

Prescriptive analytics asks:

> Is this relationship truly causal?

In other words:

- Do additional advertisements cause more clicks?
- Or is another explanation driving the pattern?

Answering this question is critical because business decisions depend on it. :contentReference[oaicite:2]{index=2}

## Alternative Explanation: Selection Bias

Advertising websites are often paid based on performance metrics such as click-through rates.

As a result, websites have incentives to identify consumers who are naturally more likely to click advertisements.

This creates a problem:

- Ads may be shown disproportionately to high-click consumers.
- Those consumers may click regardless of the advertisement.
- The observed relationship may not be caused by the ads themselves.

This phenomenon is known as **selection bias**. :contentReference[oaicite:3]{index=3}

## A Better Experiment

To investigate the issue, a different analysis was performed.

The researchers examined consumers who had already visited the advertiser's website.

This indicates:

- Strong purchase interest already exists.
- Consumers are already considering the product.

Only after this visit were additional advertisements displayed repeatedly across different websites. :contentReference[oaicite:4]{index=4}

## What the Results Showed

### First Advertisement

When consumers moved from:

- No advertisement exposure → One advertisement exposure

there was a noticeable increase in click-through rates.

Possible reasons:

- Reminder effect.
- Product awareness.
- Returning to an abandoned shopping cart.

This suggests that the first advertisement may have some genuine impact. :contentReference[oaicite:5]{index=5}

### Additional Advertisements

However, when more advertisements were shown:

- Two websites.
- Three websites.
- Four websites.
- More channels.

The click-through rate did not continue increasing.

Instead:

- CTR returned to roughly the previous level.
- Additional advertisements created little or no extra effect.

This suggests diminishing returns from repeated ad exposure. :contentReference[oaicite:6]{index=6}

## The Attribution Problem

This finding reveals a major challenge known as **attribution**.

### Attribution

Attribution attempts to determine:

- Which advertisement influenced behavior.
- Which marketing channel deserves credit.
- Whether advertising actually caused the outcome.

Without proper attribution, companies may incorrectly conclude that more advertising automatically improves performance. :contentReference[oaicite:7]{index=7}

## Correlation vs. Causation

The advertising example highlights the difference between:

### Correlation

Two variables move together.

Example:

- More advertisements are associated with higher click rates.

### Causation

One variable directly causes changes in another.

Example:

- Additional advertisements directly increase clicking behavior.

The observed data showed correlation, but further analysis suggested that the causal effect was much weaker than initially assumed. :contentReference[oaicite:8]{index=8}

## Why Descriptive Data Can Be Dangerous

A common mistake is assuming that descriptive relationships automatically represent reality.

Examples:

### Pricing Example

Observed relationship:

- Lower price → Higher demand.

### Advertising Example

Observed relationship:

- More ads → Higher CTR.

While these patterns may be true within the observed data, they do not automatically prove causation.

Other hidden factors may influence the outcome. :contentReference[oaicite:9]{index=9}

## Why Experiments Matter

To establish causality, businesses often need controlled experiments.

Examples include:

### A/B Testing

Randomly show advertisements to one group but not another.

### Randomized Experiments

Randomly assign treatments to consumers.

### Alternative Models

Test competing explanations and compare results.

These methods help determine whether an observed relationship truly reflects cause and effect. :contentReference[oaicite:10]{index=10}

## Competition and Strategic Behavior

The lecture also reinforces an earlier lesson:

Businesses do not operate in isolation.

Companies must consider:

- Competitor responses.
- Advertising incentives.
- Consumer behavior.
- Platform incentives.

These factors can distort observed data and affect optimal decisions. :contentReference[oaicite:11]{index=11}

## Related Academic Fields

Several disciplines study these problems:

### Consumer Theory
Studies pricing, demand, and consumer decision-making.

### Game Theory
Studies strategic interactions among competing firms.

### Industrial Organization (IO)
:contentReference[oaicite:12]{index=12}

Focuses on:

- Market competition.
- Firm behavior.
- Consumer interactions.
- Strategic decision-making.

These fields provide the theoretical foundations for many prescriptive analytics techniques. :contentReference[oaicite:13]{index=13}

## Key Takeaway

Prescriptive analytics requires more than identifying patterns in data. Analysts must distinguish between correlation and causation before recommending actions. The advertising example demonstrates that although consumers exposed to more advertisements appear to click more often, this relationship may be driven by selection bias rather than advertising effectiveness. To avoid incorrect decisions, businesses must use experiments, causal analysis, and alternative models to validate their assumptions. Effective prescriptive analytics therefore depends not only on data and optimization but also on understanding the true causes behind observed behavior. :contentReference[oaicite:14]{index=14}