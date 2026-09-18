---

# FILE 5 — `Data/README.md`

This is what I recommend if you **do not want to publicly upload the Excel assessment dataset**.

```markdown
# Dataset

The Power BI project was developed using a retail performance dataset containing sales, returns, customer, product, salesperson, region and target information.

The original dataset is not included in this public repository because it was provided as part of the case study/assessment and redistribution rights have not been established.

## Dataset Structure

The source data contains the following main tables:

- FactSales
- FactReturns
- FactTargets
- DimCustomer
- DimProduct
- DimSalesperson

The Power BI model also uses:

- DimDate
- DimRegion

## Data Grain

### Sales

One row represents one product line within an order.

### Returns

One row represents one returned product-line reference.

### Targets

One row represents one region-month target.

## Data Quality Issues

The original dataset intentionally contained:

- One duplicated sales record
- One missing DiscountPct value

These issues were identified and handled during the data preparation process.

## Reproducibility

The `.pbix` file contains the completed Power BI model and report.

Because the source dataset is not publicly redistributed, users who want to reproduce the analysis would need access to the original case-study dataset or an equivalent dataset with the same structure.
```
