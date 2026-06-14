# Operations Analytics - Session 4: Forecasting New Products and Fitting Demand Distributions

Forecasting new products is one of the most difficult challenges in operations analytics because there is little or no historical demand data available. Traditional forecasting methods such as moving averages and exponential smoothing rely on past observations, but new products do not have enough demand history. Therefore, organizations often begin with **subjective forecasting methods**.

Common subjective forecasting approaches include:

* **Sales Force Composite:** Sales representatives estimate future demand and the estimates are combined.
* **Customer Surveys:** Potential customers are asked about their purchasing intentions.
* **Jury of Executive Opinion:** A group of experienced managers collectively develops a forecast.
* **Delphi Method:** Experts independently provide forecasts, review the group's responses, and repeatedly revise their estimates until a consensus is reached.

Although these methods provide an initial forecast, they are often based on judgment and experience rather than objective data.

The session uses an outdoor apparel company called **Andes Inc.** as an example. Andes introduced a new men's hiking shoe called **Drifter**. Since the product had only been sold for one season, very little demand information existed. The previous forecast was 1,200 units, production was 1,500 units, and sales reached 1,397 units. Because demand history is limited, the company needs another way to estimate future demand uncertainty.

A useful idea is to learn from forecasting performance on other products. Andes has historical data for many existing shoe products, including forecasts and actual demand. By comparing forecasts with actual demand, the company can measure how accurate its forecasting process has been in the past.

An important metric introduced is the **A/F Ratio (Actual-to-Forecast Ratio)**:

[
A/F = \frac{\text{Actual Demand}}{\text{Forecast}}
]

This ratio measures forecast accuracy.

Examples:

* A/F = 1.00 → Forecast was perfectly accurate.
* A/F = 0.80 → Actual demand was only 80% of forecast.
* A/F = 1.20 → Actual demand was 20% higher than forecast.

By calculating A/F ratios for many past products, the company can understand the typical uncertainty around forecasts.

The session also highlights the difference between **sales** and **true demand**. Sales may be lower than demand when inventory runs out. This is called **censored demand**. For example, if actual demand is 1,000 units but only 800 units are available, sales will be recorded as 800 even though true demand was higher. For inventory decisions, companies need the true demand distribution rather than sales alone.

To forecast a new product, Andes starts with a subjective forecast of 1,000 units for Drifter. Historical A/F ratios are then analyzed. Suppose:

* Mean A/F Ratio = 1.01
* Standard Deviation of A/F Ratios = 0.31

The demand distribution is estimated as:

* Mean Demand = Forecast × Mean A/F Ratio
  = 1,000 × 1.01 = **1,010**

* Standard Deviation = Forecast × Standard Deviation of A/F Ratio
  = 1,000 × 0.31 = **310**

Thus, Drifter's demand can be modeled using a **Normal Distribution** with:

* Mean = **1,010**
* Standard Deviation = **310**

For predictive purposes, the standard deviation may be adjusted further to account for forecasting uncertainty, increasing from 310 to approximately 390 in this example.

The key lesson is that even when a new product has very little historical data, organizations can estimate demand uncertainty by studying forecast errors from similar products. Tracking forecast errors helps quantify uncertainty, improve forecasting accuracy, detect bias, and build realistic demand distributions for future decision-making.
