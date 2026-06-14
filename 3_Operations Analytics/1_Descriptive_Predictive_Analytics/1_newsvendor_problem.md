# Operations Analytics - Session 1: Newsvendor Problem, Forecasting, and Demand Distributions

Operations decisions are often made under uncertainty. One of the most important challenges in operations is deciding how much inventory to order or produce before actual customer demand is known. This challenge is known as the **Newsvendor Problem**.

The Newsvendor Problem involves making a single decision—how many units to order—before future demand is observed. If too many units are ordered, unsold inventory results in losses. If too few units are ordered, potential sales and profits are lost. For example, a retailer purchases a product for 3 units of currency and sells it for 12 units. If demand is high and only a small quantity is ordered, sales opportunities are missed. If demand is low and excess inventory remains unsold with no salvage value, the retailer loses money on the leftover stock.

Past demand data helps managers make better decisions. Historical demand often varies significantly, showing that future demand is uncertain. This uncertainty makes forecasting essential. The goal of forecasting is to estimate future demand so that better decisions can be made today regarding inventory, production, staffing, and capacity planning.

The Newsvendor framework appears in many real-world situations. Time Magazine faced this problem when deciding how many magazines to print and distribute before actual demand was known. By improving its forecasting and allocation decisions, the company reportedly saved approximately $3.5 million annually. Similar problems occur when governments order flu vaccines before the flu season, consumers select mobile data plans before knowing future usage, or people purchase health insurance before knowing future medical expenses.

A key lesson in forecasting is that a single-number forecast is usually inaccurate because demand is uncertain. Instead, forecasts should describe both the expected outcome and the uncertainty around it. This is commonly done using **probability distributions**.

A probability distribution represents different possible demand scenarios and the likelihood of each scenario occurring. For example, demand might be:

* High demand: 80 units with 20% probability
* Normal demand: 50 units with 70% probability
* Low demand: 20 units with 10% probability

Such a distribution is called a **discrete probability distribution** because it contains a finite set of scenarios with associated probabilities. The probabilities must always add up to 1.

Two important measures summarize a probability distribution:

**Mean (Expected Value):** The average demand expected over many future periods. In the example above, the expected demand is 53 units.

**Standard Deviation:** Measures how much actual demand is likely to vary around the mean. A larger standard deviation indicates greater uncertainty and variability.

When there are many possible outcomes, continuous probability distributions are used instead of discrete distributions. The most common example is the **Normal Distribution**, which has a bell-shaped curve and is completely described by its mean and standard deviation. Other commonly used distributions include the Exponential and Beta distributions.

Forecasting methods can be either **subjective** or **objective**. Subjective methods include sales-force estimates, customer surveys, executive opinions, and the Delphi method. Objective methods rely on historical data and are typically classified as **causal models**, which relate demand to influencing factors, and **time-series models**, which identify patterns such as trends, seasonality, cycles, and randomness in past data to predict future outcomes.

Understanding uncertainty, probability distributions, and forecasting forms the foundation for making effective operational decisions in uncertain environments.
