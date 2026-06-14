# Operations Analytics : Optimization Modeling and Resource Allocation

This session introduces **optimization**, a fundamental analytics technique used to identify the best decision when uncertainty is low and business data is known with reasonable certainty. Unlike forecasting, which predicts future outcomes, optimization focuses on choosing the best action among many alternatives.

The session uses a manufacturing company called **Zooter** as an example. Zooter produces two scooter models: **Razor** and **Navajo**. Each scooter generates profit and consumes limited manufacturing resources. Razor contributes **$150 profit per unit**, while Navajo contributes **$160 profit per unit**. However, both products require different amounts of frame manufacturing, wheels and deck assembly, and quality assurance (QA) resources.

For one Razor scooter, the company requires:

* 4 hours of frame manufacturing
* 1.5 hours of wheels and deck assembly
* 1 hour of QA and packaging

For one Navajo scooter, the company requires:

* 5 hours of frame manufacturing
* 2 hours of wheels and deck assembly
* 0.8 hours of QA and packaging

The company has limited weekly capacity:

* 5,610 frame manufacturing hours
* 2,200 wheels and deck assembly hours
* 1,200 QA and packaging hours

The goal is to determine how many Razor and Navajo scooters should be produced to maximize profit while staying within these resource limits.

The session introduces the three building blocks of every optimization model:

### 1. Decision Variables

Decision variables represent choices that managers control.

For Zooter:

* **R = Number of Razor scooters produced**
* **N = Number of Navajo scooters produced**

A specific combination of R and N is called a **solution**.

### 2. Objective Function

The objective is what the company wants to maximize or minimize.

In this case, Zooter wants to maximize profit:

[
Profit = 150R + 160N
]

This formula is called the **objective function** because it expresses profit as a function of the decision variables.

### 3. Constraints

Constraints represent limitations on available resources.

Frame Manufacturing Constraint:

[
4R + 5N \leq 5610
]

Wheels and Deck Assembly Constraint:

[
1.5R + 2N \leq 2200
]

QA and Packaging Constraint:

[
R + 0.8N \leq 1200
]

A solution satisfying all constraints is called a **feasible solution**. If even one constraint is violated, the solution becomes **infeasible**.

Additional constraints include:

* Decision variables must be non-negative.
* Decision variables must be integers because fractional scooters cannot be produced.

The complete set of objective and constraints is called an **algebraic optimization model**.

The session also introduces the concept of **linear models**. A model is linear when it contains only constants, addition, subtraction, and multiplication of decision variables by constants. Linear models are generally easier to solve using optimization software.

In contrast, **nonlinear models** contain products of decision variables, ratios, powers, roots, or other nonlinear relationships. These models are significantly more difficult to optimize, especially when the number of variables and constraints is large.

Another important insight is that an optimization model can have many decision variables and constraints, but only **one objective function**. If a company cares about multiple performance measures, one metric is chosen as the objective while the others are incorporated as constraints.

The key takeaway is that optimization problems are built using decision variables, an objective function, and constraints. Once the algebraic model is created, optimization tools such as **Solver** can systematically search through thousands or millions of possible solutions and identify the best feasible decision. This framework forms the foundation for resource allocation, production planning, supply chain management, and many other business decision-making problems.
