# Operations Analytics - Week 2 Review Session: Resource Allocation and Network Optimization

This review session reinforces the optimization concepts learned in Week 2 through two practical examples: a **resource allocation problem** and a **network optimization problem**. Both examples use the same optimization framework of **decision variables, objective function, and constraints**.

## Resource Allocation Example: Disaster Relief Housing

A UN relief agency must build temporary housing for victims of a natural disaster. Four housing types (A, B, C, and D) are available. Each housing type requires different amounts of resources such as bricks, iron sheets, wooden poles, and labor hours. Each housing type also shelters a different number of people. The agency has limited resources and wants to maximize the number of people who receive shelter.

The first step is defining **decision variables**:

* NA = Number of Type A houses
* NB = Number of Type B houses
* NC = Number of Type C houses
* ND = Number of Type D houses

The **objective function** is to maximize the total number of people housed. Each housing type contributes a certain number of shelter spaces, and the total sheltered population is calculated by multiplying the number of units built by their shelter capacities and then summing the results.

The model must also satisfy several **resource constraints**:

### Brick Constraint

Total bricks required by all housing units cannot exceed 1.5 million available bricks.

### Iron Sheet Constraint

Total iron sheets required cannot exceed 100,000 available sheets.

### Wooden Pole Constraint

Total wooden poles required cannot exceed 125,000 available poles.

### Labor Hour Constraint

Total labor hours required cannot exceed 1.5 million available labor hours.

In addition, the numbers of housing units must be **non-negative integers**, since fractional houses cannot be built.

The optimization model is then implemented in Excel using:

* Decision variable cells
* SUMPRODUCT for the objective function
* SUMPRODUCT for resource requirements
* Solver to maximize the objective

The optimized solution showed that most resources should be allocated to **Type D and Type B housing units**, with very few Type C units and no Type A units. Although Type A housed many people, it consumed too many resources compared to the other alternatives.

## Network Optimization Example: Columbia Parquet

The second example focuses on transportation and distribution planning.

A hardwood flooring company operates:

* Plant A
* Plant B

The company supplies products to:

* Region 1
* Region 2
* Region 3

Each plant has a maximum production capacity, and each region has a minimum demand requirement. Shipping between plants and regions incurs transportation costs. The company's goal is to find the lowest-cost shipping plan while satisfying all demand requirements and staying within production capacities.

The **decision variables** represent shipment quantities from each plant to each region.

Since there are:

* 2 Plants
* 3 Regions

There are:

[
2 \times 3 = 6
]

shipment variables.

The **objective function** minimizes total shipping cost. Each shipment quantity is multiplied by its transportation cost, and all costs are added together. Excel's **SUMPRODUCT** function is used to calculate this efficiently.

The model contains two types of constraints:

### Supply Constraints

The total shipments from each plant cannot exceed that plant's production capacity.

### Demand Constraints

Each region must receive at least its required minimum demand.

Unlike the housing problem, shipment quantities do not need to be integers because fractional quantities can be shipped. However, shipment quantities must remain non-negative.

The spreadsheet model is built using:

* Decision variable cells
* SUMPRODUCT objective function
* Capacity calculations
* Demand calculations
* Solver minimization

Solver automatically adjusts shipment quantities until it finds the lowest transportation cost that satisfies all capacity and demand requirements.

## Key Takeaways

1. Every optimization problem consists of:

   * Decision Variables
   * Objective Function
   * Constraints

2. Resource allocation problems focus on distributing limited resources to maximize a benefit such as profit, output, or people served.

3. Network optimization problems focus on moving products through a network at the lowest possible cost.

4. Excel's **SUMPRODUCT** function is the primary tool for calculating objective functions and resource usage.

5. **Solver** searches through possible solutions and identifies the best feasible decision.

6. Some optimization problems require integer decision variables (houses, products, employees), while others allow fractional values (tons shipped, gallons transported, square feet supplied).

7. The same optimization framework can be applied to disaster relief, logistics, supply chains, manufacturing, transportation, retail operations, and many other real-world business problems.
