# Operations Analytics : Spreadsheet Optimization Using Solver

This session explains how to convert an algebraic optimization model into a spreadsheet model and solve it using Excel's **Solver** tool. The same Zooter scooter manufacturing example from the previous session is used to demonstrate the complete optimization process.

The optimization model consists of three core components: **decision variables, objective function, and constraints**. In the Zooter case, the decision variables are the number of **Razor scooters (R)** and **Navajo scooters (N)** to produce. These values are placed in dedicated spreadsheet cells so Solver can change them during optimization.

The objective is to maximize profit. Instead of manually calculating profit for every possible production plan, a formula is created that automatically computes profit based on the decision variable values. For example, producing 500 Razor and 500 Navajo scooters generates a profit of $155,000. Whenever the decision variables change, the profit value updates automatically.

A key Excel function introduced in this session is **SUMPRODUCT**. This function multiplies corresponding values from two ranges and then adds the results together. Rather than writing long formulas manually, SUMPRODUCT provides a compact and efficient way to calculate profits and resource consumption. This becomes extremely useful when optimization models contain hundreds or thousands of variables.

The next step is modeling constraints. For every resource, the spreadsheet calculates the amount required by a production plan and compares it with the available capacity. In the Zooter example, constraints are created for:

* Frame Manufacturing Hours
* Wheels and Deck Assembly Hours
* QA and Packaging Hours

The spreadsheet continuously checks whether resource usage exceeds available capacity. Any production plan that satisfies all constraints is called a **feasible solution**, while a plan violating even one constraint is called an **infeasible solution**.

Another important Excel concept introduced is **absolute cell referencing (cell anchoring)**. By using dollar signs ($), certain cell references remain fixed when formulas are copied to other cells. This greatly simplifies building large optimization models because formulas can be copied instead of recreated repeatedly.

Once the spreadsheet model is complete, Solver is configured by specifying:

1. The **objective cell** (profit).
2. The **decision variable cells** (number of scooters).
3. The **constraints** (resource limits).
4. Integer requirements for decision variables.
5. Non-negativity requirements (cannot produce negative scooters).

Solver then searches through thousands of possible production combinations and identifies the best feasible solution much faster than manual trial and error.

For the Zooter problem, Solver finds the optimal production plan:

* **840 Razor scooters**
* **450 Navajo scooters**

This generates the maximum possible profit of **$198,000** while satisfying all resource limitations.

The session also explains common Solver messages. If Solver reports that the objective value does not converge, it usually means an important constraint is missing and the objective can increase indefinitely. If Solver reports that no feasible solution exists, it usually means that some constraints conflict with one another and cannot be satisfied simultaneously.

The main lesson is that spreadsheet optimization follows a structured process: build decision variables, create the objective function, model constraints, and allow Solver to search for the best feasible solution. This approach can be applied not only to small examples like Zooter but also to large real-world resource allocation and planning problems involving thousands of variables and constraints.
