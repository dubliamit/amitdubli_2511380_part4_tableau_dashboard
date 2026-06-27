# amitdubli_2511380_part4_tableau_dashboard
Part 4: Tableau Executive Dashboard &amp; Data Storytelling

# Retail Performance & Business Insights Dashboard

## Business Problem Summary

Retail leadership requires a centralized executive dashboard to monitor overall business performance and identify opportunities for growth while minimizing operational risks. The dashboard enables decision-makers to analyze sales performance, profitability, customer behavior, shipping efficiency, discount impact, and return patterns in a single view.

The objective is to transform transactional retail data into actionable business insights that support strategic decision-making.

---

# Dataset Description

The dataset contains retail order transactions with information related to:

* Order ID
* Customer ID
* Customer Segment
* Product Category
* Region
* Order Date
* Ship Date
* Ship Mode
* Sales
* Profit
* Discount
* Return Flag

The dataset was imported into Tableau and used to build calculated fields, visualizations, and an executive dashboard.

---

# Tableau Workbook Description

The Tableau workbook contains:

* Executive KPI cards
* Monthly Sales Trend analysis
* Shipping Performance analysis
* Discount vs Profit analysis
* Customer Segment comparison
* Return Analysis by Category and Region
* Interactive dashboard with filters

The workbook is designed to provide leadership with a high-level overview while allowing users to explore specific business areas.

---

# Calculated Fields Created

The following calculated fields were created in Tableau:

### Profit Margin
SUM([Profit]) / SUM([Sales])

### Average Order Value
SUM([Sales]) / COUNTD([Order ID])

### Return Rate
SUM([Return Flag]) / COUNT([Return Flag])

### Delivery Days
DATEDIFF('day',[Order Date],[Ship Date])

### Shipping Delay Bucket
IF [Delivery Days] <=2 THEN "0–2 Days"
ELSEIF [Delivery Days] <=5 THEN "3–5 Days"
ELSEIF [Delivery Days] <=7 THEN "6–7 Days"
ELSE "8+ Days"
END

---

# Dashboard Components

The dashboard includes the following components:

### KPI Cards

* Total Sales
* Total Profit
* Total Orders
* Total Customers
* Profit Margin
* Return Rate

### Charts

* Monthly Sales Trend (Line Chart)
* Shipping Performance (Stacked Bar Chart)
* Discount vs Profit (Scatter Plot with Trend Line)
* Customer Segment Performance (Bar Chart)
* Return Analysis by Category and Region (Bar Chart)

---

# Filters and Interactions Used

The dashboard supports interactive analysis through Tableau filters.

Possible filters include:

* Region
* Category
* Customer Segment
* Ship Mode
* Date

Interactive features:

* Highlighting
* Tooltips
* Cross-filtering between dashboard charts
* Dashboard actions for exploring specific business areas

---

# Key Business Insights

The dashboard highlights several important business findings:

* Overall sales and profit remain healthy with a profit margin of approximately 15%.
* Monthly sales are generally stable, with a sharp decline in the final reporting month that requires validation.
* Home Office customers generate the highest sales among all customer segments.
* Profit decreases as discounts increase, indicating aggressive discounting reduces profitability.
* Standard Class shipping experiences the highest volume of delayed deliveries.
* Furniture products have the highest return rates, particularly in the East region.
* Technology products maintain stronger profitability than other product categories.
* Shipping efficiency and return reduction present opportunities for improving customer satisfaction and overall profit.

---

# Dashboard Story Summary

The dashboard tells a connected business story rather than presenting isolated charts.

It begins with an executive overview of key performance indicators before examining sales trends over time. It then explores operational performance through shipping analysis, identifies profitability drivers using discount analysis, compares customer segment performance, and concludes with return analysis to highlight operational risks.

Together, these visualizations help leadership understand current business performance, identify emerging risks, and prioritize improvement initiatives.

---

# Assumptions and Limitations

## Assumptions

* Return Flag values are encoded as:

  * 1 = Returned
  * 0 = Not Returned
* Ship Date occurs after Order Date.
* Sales and Profit values are complete and accurate.
* All orders contain valid customer and product information.

## Limitations

* Customer lifetime value is not included.
* Inventory and stock availability are not analyzed.
* Marketing campaign performance is outside the scope of the dashboard.
* Root causes of returns cannot be determined from transactional data alone.
* The unusually low sales value in the final month may represent incomplete data rather than actual business performance.

---

# Screenshots Included

Repository includes screenshots of:

* Executive Dashboard
* Sales trend chart
* Regional or state-level performance
* Category/sub-category profitability
* Evidence of filter or dashboard interaction

---

# Tools Used

* Tableau Desktop
* Tableau Calculated Fields
* Interactive Dashboards
* Data Visualization Best Practices

---

# Conclusion

This Tableau dashboard provides retail leadership with a comprehensive view of business performance by combining financial metrics, operational efficiency, customer insights, and return analysis into a single interactive reporting solution. The dashboard supports informed decision-making by identifying growth opportunities, operational bottlenecks, and profitability risks.
