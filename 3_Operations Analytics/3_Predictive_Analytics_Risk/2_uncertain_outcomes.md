# Operations Analytics - Week 3, Session 2: Simulation Modeling and Estimating Reward and Risk

In the previous session, decision-making under uncertainty was introduced through the concepts of **reward** and **risk**. This session explains how to estimate these measures using **simulation**, a powerful analytics tool that converts uncertain inputs into uncertain outputs and helps evaluate business decisions when future outcomes cannot be predicted with certainty.

The session continues with the wireless data plan example. The current plan charges **$10 per gigabyte** of data usage. The new plan charges a **fixed fee of $160 for up to 20 GB** and then **$15 for every additional gigabyte above 20 GB**. Historical analysis suggests that monthly data usage follows a **Normal Distribution** with:

* Mean = 23 GB
* Standard Deviation = 5 GB

The challenge is to estimate the probability distribution of monthly payments under the new plan and determine its reward and risk characteristics.

The first step is creating an algebraic model that links the uncertain input (monthly data usage) to the uncertain output (monthly payment). If monthly usage is less than or equal to 20 GB, payment is simply $160. If usage exceeds 20 GB, an additional charge is applied:

[
Payment = 160 + 15(Usage - 20)
]

This relationship can be represented in Excel using the **IF function**, which automatically selects the appropriate payment formula based on the simulated data usage value.

A critical lesson of this session is that expected values cannot always be estimated by simply replacing random variables with their averages. For example, substituting the expected data usage value of 23 GB into the payment formula gives a payment estimate of $205. However, this does not necessarily equal the true expected payment. Nonlinear relationships between inputs and outputs often make this shortcut inaccurate. Therefore, simulation is needed to estimate reward and risk correctly.

Simulation works through repeated **simulation runs**. During each run:

1. A random data usage value is generated from the Normal distribution.
2. The payment formula converts that data usage value into a monthly payment.
3. The resulting payment is stored as one observation in the simulation output.

Repeating this process many times creates a sample of possible future outcomes. The collection of generated usage values is called the **input sample**, while the resulting payment values form the **output sample**.

The session demonstrates how to implement simulation in Excel using the **Analysis ToolPak**. The Random Number Generation tool is configured to generate ten random monthly usage values from a Normal distribution with mean 23 and standard deviation 5. Each generated value is then passed through the payment formula to calculate a corresponding monthly payment. This produces ten simulated payment outcomes.

Once the simulation output is generated, reward and risk measures can be estimated using descriptive statistics:

### Reward Measure

The **sample mean** of the simulated payment values estimates the expected monthly payment.

### Risk Measure

The **sample standard deviation** of the simulated payment values estimates the variability and uncertainty of monthly payments.

For the ten-run simulation presented in the session:

* Estimated Reward (Average Monthly Payment) ≈ **$253**
* Estimated Risk (Standard Deviation of Payments) ≈ **$92**

These values provide an initial estimate of how attractive and risky the new data plan may be.

The key takeaway is that simulation transforms uncertain inputs into uncertain outputs, allowing managers to estimate reward and risk for any decision. By generating many possible future scenarios and analyzing the resulting outcomes, simulation provides a practical way to evaluate decisions when analytical calculations are difficult or impossible. This simulation framework forms the foundation for comparing alternatives and making better decisions under uncertainty.
