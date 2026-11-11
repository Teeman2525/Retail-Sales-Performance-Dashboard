# Retail Sales Performance Dashboard | Power BI

## Project Overview

This project presents an interactive two-page Power BI dashboard analyzing retail sales performance in 2025. The dashboard helps stakeholders monitor revenue, profitability, order activity, sales channels, product performance, and regional trends.

The report combines key performance indicators (KPIs), DAX calculations, and interactive filters to support data-driven business decisions.

## Dashboard Preview

### Page 1 — Executive Overview

![Executive Overview](Executive%20Overview.jpg)

### Page 2 — Product & Regional Analysis

![Product and Regional Analysis](Product%20%26%20Regional%20Analysis.jpg)

## Tools and Technologies

- Microsoft Power BI Desktop
- Power Query
- DAX (Data Analysis Expressions)
- Data Modeling
- Interactive Data Visualization

## Key Performance Indicators

| Metric | Value |
|---|---|
| Total Revenue | $541.93K |
| Total Profit | $215.72K |
| Profit Margin | 39.81% |
| Total Orders | Approximately 1,000 |
| Units Sold | Approximately 3,000 |

## DAX Measures

**Total Profit**
```dax
Total Profit =
SUMX(
    SalesTransactions,
    (SalesTransactions[Unit Price] - SalesTransactions[Unit Cost])
    * SalesTransactions[Quantity]
)
```

**Total Orders**
```dax
Total Orders =
DISTINCTCOUNT(SalesTransactions[Order ID])
```

**Units Sold**
```dax
Units Sold =
SUM(SalesTransactions[Quantity])
```

**Profit Margin**
```dax
Profit Margin =
DIVIDE([Total Profit], [Total Revenue], 0)
```

## Key Business Insights

1. **Revenue Performance:** The business generated approximately $541.93K in revenue and $215.72K in profit, with a profit margin of 39.81%.

2. **Monthly Revenue:** June recorded the highest monthly revenue, suggesting a period worth investigating for promotional or seasonal influences.

3. **Regional Performance:** The East region generated approximately $78K in revenue, making it the strongest-performing region.

4. **Sales Channels:** Retail Store contributed approximately 36.01% of total revenue. A small proportion (0.24%) was recorded under an Unknown sales channel, highlighting a data-quality issue.

5. **Product Performance:** Printer Paper generated approximately $64K, making it the highest-revenue product.

6. **Category Profitability:** Office Supplies generated approximately $54K in profit, outperforming the other product categories.

## Business Recommendations

- Investigate the factors contributing to June's revenue peak to identify repeatable growth opportunities.
- Study successful sales strategies in the East region and assess whether they can be applied elsewhere.
- Review high-revenue products alongside their profitability before making inventory and promotional decisions.
- Investigate and correct Unknown sales-channel records to improve reporting accuracy.
- Monitor category-level profit margins to guide product and pricing strategies.

## Project Features

- Two-page interactive dashboard
- Dynamic KPI cards
- Region and sales-channel filters
- Year filtering
- Monthly revenue trend analysis
- Product and regional comparisons
- Category profitability analysis

## How to Explore the Project

1. Download the `.pbix` file from this repository.
2. Open it using Microsoft Power BI Desktop.
3. Navigate between the Executive Overview and Product & Regional Analysis pages.
4. Use the interactive filters to explore different sales segments.

## Project Note

This project was completed as part of my practical data analytics learning and portfolio development. The analysis, DAX measures, dashboard development, and interpretation of results were carried out as part of my hands-on training.

## Author

**Teeman**  
Aspiring Data Analyst | Computer Engineering | IT Support
