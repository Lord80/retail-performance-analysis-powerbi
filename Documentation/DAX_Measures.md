---

# FILE 4 — `Documentation/DAX_Measures.md`

This one is important because it demonstrates that you actually understand what you built.

Use this:

```markdown
# DAX Measures

## Overview

The Power BI report uses DAX measures to create reusable business calculations.

The measures are designed to respond dynamically to slicers, filters and visual context.

---

# Sales Measures

## Net Sales

Net Sales represents sales value after applying the relevant discount.

Conceptually:

```DAX
Net Sales =
SUMX(
    FactSales_Raw,
    FactSales_Raw[Quantity] *
    FactSales_Raw[UnitPrice] *
    (1 - FactSales_Raw[DiscountPct])
)

Gross Profit =
[Net Sales] - [Total Cost]

Gross Margin % =
DIVIDE(
    [Gross Profit],
    [Net Sales]
)

Total Quantity =
SUM(FactSales_Raw[Quantity])

Total Orders =
DISTINCTCOUNT(FactSales_Raw[OrderID])

Average Order Value =
DIVIDE(
    [Net Sales],
    [Total Orders]
)

Returned Quantity =
SUM(FactReturns[ReturnedQuantity])

Return Rate % =
DIVIDE(
    [Returned Quantity],
    [Total Quantity]
)

Target Sales =
SUM(FactTargets[TargetSales])

Target Variance =
[Net Sales] - [Target Sales]

Target Variance % =
DIVIDE(
    [Target Variance],
    [Target Sales]
)

Target Attainment % =
DIVIDE(
    [Net Sales],
    [Target Sales]
)

Customer Sales =
[Net Sales]

Customer Sales % of Company =
DIVIDE(
    [Customer Sales],
    CALCULATE(
        [Customer Sales],
        ALLSELECTED(DimCustomer)
    )
)

Customer Sales Rank =
RANKX(
    ALLSELECTED(DimCustomer),
    [Customer Sales],
    ,
    DESC,
    DENSE
)

Salesperson Sales =
[Net Sales]

Salesperson AOV =
DIVIDE(
    [Salesperson Sales],
    [Total Orders]
)

Salesperson Sales Rank =
IF(
    ISINSCOPE(DimSalesperson[SalespersonName]),
    RANKX(
        ALLSELECTED(DimSalesperson),
        [Salesperson Sales],
        ,
        DESC,
        DENSE
    )
)

Selected Metric =
SWITCH(
    SELECTEDVALUE('Metric Selector'[Metric]),
    "Net Sales", [Net Sales],
    "Gross Profit", [Gross Profit],
    "Orders", [Total Orders],
    [Net Sales]
)

Top N Selector =
DATATABLE(
    "Top N", INTEGER,
    {
        {5},
        {10},
        {15}
    }
)

Selected Top N =
SELECTEDVALUE(
    'Top N Selector'[Top N],
    10
)

Show Top N =
IF(
    [Selected Metric Rank] <= [Selected Top N],
    1,
    0
)



```
