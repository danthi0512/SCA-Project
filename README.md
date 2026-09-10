# Production Planning Optimization using Linear Programming

## 📌 Project Overview

This project develops a Linear Programming (LP) model to optimize production planning and inventory decisions for a manufacturing company.

The model determines how much to produce for each SKU in each month while minimizing total production and inventory holding costs, subject to production capacity and inventory constraints.

## 🎯 Business Problem

The company needs to plan production for 15 SKUs over a 12-month planning horizon.

The main challenges are:

- Different demand levels across SKUs and months
- Limited monthly production capacity
- Production costs vary by SKU
- Holding inventory incurs additional costs
- Inventory capacity is limited

The objective is to find the optimal production plan that satisfies demand at the minimum total cost.

## 🧮 Optimization Model

### Decision Variables

**Production quantity**

$$
X_{p,t} = \text{quantity of SKU } p \text{ produced in month } t
$$

**Ending inventory**

$$
I_{p,t} = \text{ending inventory of SKU } p \text{ in month } t
$$

### Objective

Minimize total production and inventory holding costs:

$$
\min \sum_{p,t}
(C_p X_{p,t} + H_p I_{p,t})
$$

### Key Constraints

**Inventory balance**

$$
I_{p,t-1} + X_{p,t} - D_{p,t} = I_{p,t}
$$

**Production capacity**

$$
\sum_p T_p X_{p,t} \leq Capacity_t
$$

**Inventory capacity**

$$
I_{p,t} \leq MaxInventory_p
$$

## 🛠️ Tools & Technologies

- Python
- Pandas
- PuLP
- Matplotlib
- Linear Programming

## 📊 What-if Scenario Analysis

The model will be extended to evaluate different business scenarios, such as:

- Demand increase/decrease
- Production capacity changes
- Changes in inventory holding costs

The objective is to understand how changes in business assumptions affect the optimal production plan, inventory levels, and total cost.
