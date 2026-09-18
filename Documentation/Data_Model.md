# Data Model

## Overview

The Power BI solution uses a star-schema-oriented data model.

The model separates transactional fact tables from descriptive dimension tables.

This structure allows the same business dimensions to be used consistently across sales, returns and target analysis.

---

# Fact Tables

## FactSales

### Grain

One row represents one product line within an order.

This means an order can contain multiple rows.

For example, a single order may contain several different products.

Therefore, raw row count should not be used as the number of orders.

### Main fields

- OrderID
- OrderDate
- CustomerID
- ProductID
- SalespersonID
- Quantity
- UnitPrice
- DiscountPct

### Main analytical uses

- Net Sales
- Gross Profit
- Gross Margin
- Orders
- Quantity
- AOV
- Customer analysis
- Product analysis
- Salesperson analysis

---

# FactReturns

### Grain

One row represents a returned product-line reference.

### Main analytical uses

- Returned Quantity
- Return Rate
- Returns by Reason
- Returns by Product
- Returns by Category
- Return trends

---

# FactTargets

### Grain

One row represents a target for a region-month combination.

### Main analytical uses

- Target Sales
- Target Variance
- Target Variance %
- Target Attainment %
- Monthly target analysis
- Regional target analysis

---

# Dimension Tables

## DimDate

Provides the date dimension used for time-based analysis.

Used for:

- Year
- Month
- Monthly trends
- Sales trends
- Return trends
- Target trends

---

## DimCustomer

Contains customer-level descriptive information.

Used for:

- Customer performance
- Customer ranking
- Customer contribution
- Customer concentration
- Customer drill-through

---

## DimProduct

Contains product-level descriptive information.

Used for:

- Product performance
- Category analysis
- Gross margin analysis
- Return analysis
- Product tooltip

---

## DimSalesperson

Contains salesperson-level information.

Used for:

- Salesperson sales
- Salesperson AOV
- Salesperson ranking
- Salesperson comparison

---

## DimRegion

Contains regional information.

Used for:

- Regional sales
- Regional profitability
- Target analysis
- Regional filtering

---

# Relationships

The model follows a dimension-to-fact filtering structure.

Conceptually:

```text
                 DimDate
                    |
                    v
               FactSales
              /    |    \
             /     |     \
            v      v      v
   DimCustomer  DimProduct  DimSalesperson
                         |
                         |
                    DimRegion


                 DimDate
                    |
                    v
               FactReturns
                    |
                    v
                DimProduct


                 DimDate
                    |
                    v
               FactTargets
                    |
                    v
                 DimRegion
```
