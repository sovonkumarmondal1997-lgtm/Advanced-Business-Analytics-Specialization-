# Operations Analytics - Week 3, Session 1: Decision Making Under Uncertainty, Reward, Risk, and Simulation

In the previous week, optimization problems assumed that all data was known with certainty. For every decision, managers knew exactly what profit, cost, or resource usage would result. However, many real-world business decisions occur in environments where future outcomes are uncertain. In such situations, a single decision can lead to multiple possible outcomes, making decision-making much more complex. This is where **simulation analytics** becomes important.

The session begins by contrasting **low-uncertainty environments** with **high-uncertainty environments**. In low-uncertainty settings, such as the Zooter scooter optimization example, a production decision immediately produces a known profit value and known resource consumption. The objective is simply to find the best feasible solution. In high-uncertainty settings, however, outcomes depend on random future events. Instead of producing a single outcome, a decision generates a **probability distribution of outcomes**.

The Newsvendor problem illustrates this concept. Suppose a product sells for 12 units of currency, costs 3 units to produce, and unsold inventory has no salvage value. The decision of how many units to produce must be made before actual demand is known. If 50 units are produced, profit depends entirely on future demand. For example:

* If demand is 29 units, profit equals 198.
* If demand is 41 units, profit equals 342.
* If demand is 63 units, profit equals 450.

Thus, one production decision can generate several possible profit outcomes depending on which demand scenario occurs. This means profit itself becomes a random variable rather than a fixed number.

To compare decisions under uncertainty, managers need performance measures. The first measure is **Reward**. Reward reflects how attractive a decision is and is usually measured using the **expected value** of profit or cost. For profits, higher expected profit is preferred. For costs, lower expected cost is preferred. Expected value represents the average outcome that would occur over a very large number of repetitions.

The session introduces a wireless data plan example. A consultant currently pays $10 per gigabyte of data. An alternative plan charges a fixed $160 per month for up to 20 GB, plus $15 for every GB above 20. Future monthly data usage is uncertain and is modeled as a Normal distribution with:

* Mean = 23 GB
* Standard Deviation = 5 GB

Under the current plan, monthly payment equals 10 × Usage. Since multiplying a normally distributed variable by a constant preserves normality:

* Expected Monthly Payment = $230
* Standard Deviation = $50

This gives a complete probability distribution for future monthly payments.

However, expected payment alone is insufficient because actual monthly payments may vary significantly. Therefore, managers must also evaluate **Risk**. One common risk measure is the **standard deviation**, which indicates how much actual outcomes vary around the expected value. A lower standard deviation generally indicates less uncertainty. Another risk measure might be the probability that a payment exceeds a specified threshold, such as $300. Different decision makers may define risk differently depending on their objectives.

The session concludes by presenting a framework for decision-making under uncertainty:

1. Define reward and risk performance measures.
2. Use **simulation** to estimate these measures for each decision alternative.
3. Use **optimization** to select the best alternative by maximizing reward while controlling risk through constraints.

This combination of forecasting, simulation, and optimization forms the foundation for making effective decisions in uncertain business environments.
