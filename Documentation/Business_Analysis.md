---

# FILE 2 — `Documentation/Business_Analysis.md`

This is where we put the **full Part 11 + Part 12 analysis**, instead of making the README huge.

```markdown
# Business Analysis

## Overview

This document contains the business analysis performed after building the Power BI retail performance report.

The objective was not only to describe the visuals but to answer the business questions defined in the case study and translate the findings into actionable recommendations.

---

# Part 11 — Business Analysis

## Q1. What is the strongest region, and why?

### Answer: East

East is the strongest overall region based on the combination of revenue, gross profit and target performance.

Approximate performance:

| Region | Net Sales | Target Attainment |
| ------ | --------: | ----------------: |
| East   |    $2.53M |            159.7% |
| West   |    $2.28M |            113.6% |
| South  |    $2.19M |            124.2% |
| North  |    $2.06M |            113.2% |

East leads the business in sales and gross profit and also has the highest target attainment.

It is important to note that East does not have the highest gross margin. West has a slightly higher margin.

Therefore, East should be considered the strongest overall region because of its combination of scale, profitability and target performance rather than because of margin alone.

### Business interpretation

The next question should be why East performs so strongly.

Potential drivers to investigate include:

- Customer mix
- Product mix
- Salesperson performance
- Average order value
- Discounting
- Order frequency

The current dataset shows the performance difference but does not fully explain its cause.

---

# Q2. Which product/category is strongest in revenue and gross profit?

## Category level

Furniture is the strongest category by revenue and gross profit.

Approximate results:

| Category    | Net Sales | Gross Profit | Gross Margin |
| ----------- | --------: | -----------: | -----------: |
| Furniture   |    $4.51M |       $1.56M |        34.5% |
| Electronics |    $3.98M |       $1.29M |        32.4% |
| Office      |    $0.57M |       $0.24M |        41.5% |

Furniture is therefore the largest contributor to business revenue and gross profit.

However, Office has the highest gross margin.

This distinction is important:

- Furniture = largest business contribution
- Office = highest margin efficiency

---

## Product level

Standing Desk is the strongest individual product in both revenue and gross profit.

Approximate results:

- Net Sales: $1.76M
- Gross Profit: $594.8K
- Gross Margin: 33.7%

Therefore, the highest-revenue and highest-gross-profit product are the same in this dataset.

---

# Q3. Which region has the biggest target-attainment problem?

### Answer: North

North has the lowest target attainment at approximately 113%.

West is close at approximately 114%.

However, North is still exceeding its target.

Therefore, it would be incorrect to describe North as a failed or under-target region.

The correct interpretation is:

> North has the weakest relative target performance among the regions, but it is still above target.

This distinction is important for management decision-making.

---

# Q4. Is there evidence of customer concentration risk?

The customer base appears relatively diversified.

Approximate customer contribution:

| Customer Group | Contribution |
| -------------- | -----------: |
| Top 1          |         3.1% |
| Top 3          |         9.1% |
| Top 10         |       ~24.7% |

The largest customer contributes only around 3.1% of company sales.

This suggests the company is not dependent on one or two customers.

The Pareto analysis also shows that approximately half of revenue is spread across a substantial portion of the customer base.

### Conclusion

There is some customer concentration worth monitoring, but the available evidence does not support describing the business as highly dependent on a small number of customers.

---

# Q5. Which product/category has the most concerning return behaviour?

## Product level: Filing Cabinet

Filing Cabinet has the highest product-level return rate at approximately 9.3%.

At the same time, it generates approximately $1.53M in sales.

This makes the issue more significant than a high return rate on a low-volume product.

### Why this matters

A high return rate on a commercially important product can potentially affect:

- Customer satisfaction
- Profitability
- Operational costs
- Inventory
- Fulfilment efficiency

However, the current dataset does not provide enough information to determine the root cause.

---

## Category level

Furniture has the highest category-level return rate among the major categories.

Therefore:

- Category concern → Furniture
- Individual product concern → Filing Cabinet

---

# Q6. Which salesperson performs best?

### Answer: Meera

Salesperson performance should not be judged using sales alone.

The analysis considers multiple dimensions including:

- Sales
- Gross Profit
- Average Order Value
- Gross Margin

Meera leads in sales and gross profit while also maintaining a strong AOV.

This makes her the strongest overall salesperson based on the dimensions available in this dataset.

However, Arjun has a slightly higher gross margin.

This demonstrates why salesperson performance should be evaluated across multiple metrics rather than total sales alone.

---

# Q7. Where does high sales not mean strong performance?

## Monitor 24in

Monitor 24in generates approximately $1.57M in sales.

This makes it one of the highest-revenue products.

However, its gross margin is approximately 28.8%, compared with an overall business margin of approximately 34%.

Therefore:

> High sales contribution does not automatically mean strong profitability.

The product deserves further investigation into:

- Product cost
- Discounting
- Pricing
- Customer/segment mix

The available data shows the performance outcome but does not establish the root cause.

---

# Q8. Management Recommendations

## Recommendation 1 — Investigate Filing Cabinet Returns

### Evidence

Filing Cabinet has approximately a 9.3% return rate while generating approximately $1.53M in sales.

### Problem

A commercially important product has relatively high returns.

### Recommendation

Analyze detailed return reasons and operational information to determine whether the issue is caused by:

- Product quality
- Damage
- Fulfilment errors
- Wrong item
- Customer preference
- Other operational causes

---

## Recommendation 2 — Review Monitor 24in Profitability

### Evidence

Monitor 24in generates approximately $1.57M in sales but has only approximately 28.8% gross margin.

### Problem

A high-revenue product generates below-average margin.

### Recommendation

Review:

- Product cost
- Discounting
- Pricing
- Customer mix
- Segment mix

The goal should be to identify the reason for the lower margin before deciding on a corrective action.

---

## Recommendation 3 — Investigate East's Performance Drivers

### Evidence

East leads the business in:

- Net Sales
- Gross Profit
- Target Attainment

### Problem

There is a substantial performance gap between East and the lower-performing regions.

### Recommendation

Break East's performance down by:

- Customer
- Product
- Salesperson
- Segment
- Average Order Value
- Discount

The objective is to identify repeatable practices that could potentially be applied to other regions.

---

# Part 12 — Final Professional Judgement

## What did the analysis reveal?

The business is performing strongly overall, exceeding the sales target by approximately 26%.

East is the strongest region, while Furniture and Standing Desk are major contributors to revenue and gross profit.

However, the analysis also shows that revenue alone is not enough to judge performance.

Monitor 24in has strong sales but weaker margin, while Filing Cabinet has strong sales but the highest return rate.

Customer revenue is relatively diversified, reducing the evidence for severe customer concentration risk.

---

## What was surprising?

The most important observation was that high revenue does not always translate into strong overall performance.

Two examples illustrate this:

1. Monitor 24in — high sales but relatively low margin.
2. Filing Cabinet — high sales combined with a high return rate.

This demonstrates why business analysis needs to consider multiple performance dimensions.

---

## What would I investigate next?

### 1. East

Investigate the drivers behind East's superior performance.

### 2. Monitor 24in

Investigate product cost, pricing and discounting.

### 3. Filing Cabinet

Investigate detailed return reasons and operational causes.

---

## What additional data would I request?

### Product and cost data

- Product cost
- Shipping cost
- Fulfilment cost
- Return processing cost

### Customer data

- Customer acquisition date
- Purchase history
- Customer lifetime value
- Retention
- Churn
- Acquisition channel

### Return data

- Detailed return reason
- Damage/defect indicator
- Warehouse
- Supplier
- Product batch
- Return cost
- Resolution

### Salesperson data

- Leads/opportunities
- Conversion rate
- Discounting
- Sales cycle
- New versus existing customers
- Customer retention

---

# Conclusions I Would NOT Make

A strong analyst should also identify what the data cannot prove.

## I would not conclude that East's sales team is better.

East performs better, but this could be influenced by:

- Customer mix
- Product mix
- Market conditions
- Order size
- Pricing

More evidence is required.

---

## I would not conclude that Filing Cabinet has a quality problem.

A high return rate does not automatically mean poor product quality.

Detailed return reasons are required.

---

## I would not conclude that Monitor 24in is overpriced.

Its margin is low, but the cause could be:

- Product cost
- Discounting
- Pricing
- Customer mix

The dataset does not establish the cause.

---

## I would not conclude that the business has severe customer concentration risk.

The available customer contribution analysis indicates a relatively diversified customer base.

---

## I would not say Meera is objectively the best salesperson.

Meera is the strongest salesperson based on the dimensions available in this dataset.

A definitive ranking would require additional measures such as:

- Conversion rate
- Customer retention
- Opportunity volume
- Territory difficulty
- New customer acquisition

---

# Overall Conclusion

The retail business is performing strongly against its targets, but the analysis reveals several areas where management should look beyond headline sales.

The most important opportunities for further investigation are:

1. High returns on Filing Cabinet
2. Low margin on Monitor 24in
3. Understanding the drivers behind East's exceptional performance

The key analytical lesson is:

> Revenue is an important measure of business performance, but it should be evaluated together with profitability, returns, targets, customer concentration and operational context.
