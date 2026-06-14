# Operations Analytics - Week 2, Session 3: Network Optimization

## Overview

This session introduces **Network Optimization**, a type of optimization problem where products must be transported through a network of locations at the **lowest possible cost** while satisfying supply and demand requirements.

Unlike the previous resource allocation problem (Zooter), this problem focuses on **transportation and logistics**.

---

# Business Scenario: Keystone Dry Goods Logistics

Keystone Dry Goods Logistics must transport powdered drink from:

### Warehouses (Supply Locations)

| Warehouse     | Supply (Tons) |
| ------------- | ------------- |
| Los Angeles   | 15            |
| Chicago       | 20            |
| New York City | 30            |

### Distribution Centers (Demand Locations)

| Distribution Center | Minimum Demand (Tons) |
| ------------------- | --------------------- |
| Denver              | 10                    |
| Austin              | 13                    |
| Washington D.C.     | 20                    |

The goal is to determine:

**How much product should be shipped from each warehouse to each distribution center while minimizing total transportation cost.**

---

# Three Components of the Optimization Model

## 1. Decision Variables

Decision variables represent shipment quantities between warehouses and distribution centers.

Because there are:

* 3 Warehouses
* 3 Distribution Centers

Total decision variables:

[
3 \times 3 = 9
]

Examples:

| Variable | Meaning                  |
| -------- | ------------------------ |
| XLD      | Los Angeles → Denver     |
| XLA      | Los Angeles → Austin     |
| XLW      | Los Angeles → Washington |
| XCD      | Chicago → Denver         |
| XCA      | Chicago → Austin         |
| XCW      | Chicago → Washington     |
| XND      | New York → Denver        |
| XNA      | New York → Austin        |
| XNW      | New York → Washington    |

These variables represent the number of tons shipped on each route.

---

## 2. Objective Function

### Goal: Minimize Total Shipping Cost

Each route has a shipping cost per ton.

Example:

* Los Angeles → Denver = $105 per ton
* New York → Austin = $132 per ton

If:

[
X_{LD}=10
]

Then shipping cost is:

[
105 \times 10 = 1050
]

Total cost is the sum of costs across all routes:

[
\text{Total Cost}
=================

\sum (\text{Cost per ton} \times \text{Shipment quantity})
]

The optimization model seeks the shipment plan with the **lowest total cost**.

---

## 3. Constraints

### Supply Constraints

Every warehouse must ship exactly its available inventory.

#### Los Angeles

[
X_{LD}+X_{LA}+X_{LW}=15
]

#### Chicago

[
X_{CD}+X_{CA}+X_{CW}=20
]

#### New York

[
X_{ND}+X_{NA}+X_{NW}=30
]

These ensure all available product leaves each warehouse.

---

### Demand Constraints

Each distribution center must receive at least its required amount.

#### Denver

[
X_{LD}+X_{CD}+X_{ND}\ge10
]

#### Austin

[
X_{LA}+X_{CA}+X_{NA}\ge13
]

#### Washington

[
X_{LW}+X_{CW}+X_{NW}\ge20
]

These ensure customer demand is satisfied.

---

### Non-Negativity Constraints

Shipment quantities cannot be negative:

[
X_{ij}\ge0
]

Unlike the scooter example, shipments do **not** need to be integers because fractional shipments are possible.

Example:

[
12.5 \text{ tons}
]

is acceptable.

---

# Spreadsheet Formulation in Excel

## Step 1: Create Decision Variable Cells

A 3×3 table is created representing shipments between:

* Warehouses (rows)
* Distribution Centers (columns)

These cells hold the shipment quantities.

Convention:

* Blue color
* Bold formatting

to visually identify decision variables.

---

## Step 2: Create Objective Function Cell

The total shipping cost is calculated using:

```excel
=SUMPRODUCT(Shipment_Quantities, Shipping_Costs)
```

Example:

```excel
=SUMPRODUCT(B12:D14,B6:D8)
```

SUMPRODUCT multiplies each shipment quantity by its corresponding shipping cost and sums all products.

Initial trial solution cost:

[
$11,570
]

---

## Step 3: Create Supply Constraint Calculations

For Los Angeles:

```excel
=SUM(B12:D12)
```

This calculates total shipments leaving Los Angeles.

The formula is copied for Chicago and New York.

These values are later constrained to equal available supply.

---

## Step 4: Create Demand Constraint Calculations

For Denver:

```excel
=SUM(B12,B13,B14)
```

This calculates total shipments arriving at Denver.

The formula is copied for Austin and Washington.

These values are later constrained to be greater than or equal to required demand.

---

# Configuring Solver

### Objective Cell

* Total Shipping Cost Cell
* Minimize

### Variable Cells

* Shipment Quantity Table

### Constraints

Supply:

```text
Warehouse Shipments = Available Supply
```

Demand:

```text
Distribution Center Receipts ≥ Required Demand
```

Additional Constraint:

```text
Shipment Quantities ≥ 0
```

Solver Method:

```text
GRG Nonlinear
```

Then click **Solve**.

---

# Optimal Solution

Solver finds the transportation plan with the minimum possible shipping cost.

### Optimal Cost

[
$7,485
]

This is the lowest transportation cost that satisfies all supply and demand requirements.

---

# Important Takeaways

### Resource Allocation vs Network Optimization

| Resource Allocation                 | Network Optimization         |
| ----------------------------------- | ---------------------------- |
| Allocate resources among activities | Move goods through a network |
| Example: Zooter Scooters            | Example: Keystone Logistics  |
| Maximize profit                     | Minimize transportation cost |

---

### Core Optimization Framework

Every optimization problem contains:

1. Decision Variables
2. Objective Function
3. Constraints

This framework applies whether using:

* Excel Solver
* Commercial Optimization Software
* Enterprise Analytics Platforms

---

# Real-World Applications

Network optimization is widely used in:

* Supply Chain Management
* Logistics
* Transportation Planning
* Airline Routing
* Retail Distribution
* Manufacturing Networks
* Warehouse Management

Large organizations such as:

* Chevron Corporation
* Zara

use optimization techniques to improve operations and reduce costs.

---

# Session Summary

This session introduced transportation/network optimization. A logistics company must move goods from warehouses to distribution centers at minimum cost while satisfying supply and demand requirements. The problem was modeled using decision variables, an objective function, and constraints, then solved in Excel using Solver. The optimal shipping plan achieved a minimum transportation cost of **$7,485**. The session emphasized that the same optimization framework is used in real-world logistics, supply chain, and operations management problems.
