# Chart Selection Justification

## 1. KPI Cards (Total Sales, Total Profit, Total Orders, Total Customers, Profit Margin, Return Rate)

### What question does the chart answer?

Provides an executive summary of the company's overall business performance.

### Why is the chart type appropriate?

KPI cards present the most important business metrics in a simple, highly visible format that executives can understand at a glance.

### Fields used

* **Measure:** Sales, Profit, Order ID, Customer ID, Profit Margin, Return Rate
* **Labels:** KPI names

### Design principle applied

High visual hierarchy with large fonts and minimal distractions to emphasize key performance indicators.

### Mistake avoided

Avoided combining multiple KPIs into one chart, which would reduce readability and make comparisons difficult.

---

## 2. Monthly Sales Trend (Line Chart)

### What question does the chart answer?

How has sales performance changed over time?

### Why is the chart type appropriate?

A line chart is the most effective visualization for showing trends, seasonality, and changes across time.

### Fields used

* **X-axis:** Month of Ship Date
* **Y-axis:** SUM(Sales)
* **Labels:** Monthly sales values

### Design principle applied

Chronological ordering highlights business trends and makes changes over time easy to identify.

### Mistake avoided

Avoided using a bar chart, which is less effective for displaying continuous time-series data.

---

## 3. Shipping Performance (Stacked Bar Chart)

### What question does the chart answer?

Which shipping modes experience the highest delivery delays?

### Why is the chart type appropriate?

A stacked bar chart allows comparison of shipment volume while simultaneously showing the distribution of delivery delay buckets.

### Fields used

* **X-axis:** Ship Mode
* **Y-axis:** Count of Orders
* **Color:** Shipping Delay Bucket

### Design principle applied

Color is used to separate delivery delay categories, allowing quick comparison across shipping modes.

### Mistake avoided

Avoided using a pie chart, which cannot effectively compare multiple categories across different shipping modes.

---

## 4. Discount vs Profit (Scatter Plot with Trend Line)

### What question does the chart answer?

How does discount affect profitability?

### Why is the chart type appropriate?

Scatter plots are ideal for identifying relationships, patterns, clusters, and outliers between two continuous variables.

### Fields used

* **X-axis:** Discount
* **Y-axis:** Profit
* **Color:** Category
* **Trend Line:** Linear trend

### Design principle applied

Color differentiates product categories while the trend line clearly communicates the overall relationship.

### Mistake avoided

Avoided aggregating data into bars, which would hide individual transactions and reduce visibility of the relationship.

---

## 5. Customer Segment Performance (Bar Chart)

### What question does the chart answer?

Which customer segment contributes the highest sales?

### Why is the chart type appropriate?

Bar charts provide the clearest comparison of values across discrete categories.

### Fields used

* **X-axis:** Customer Segment
* **Y-axis:** SUM(Sales)
* **Labels:** Sales values
* **Filter:** Customer Segment

### Design principle applied

Simple vertical bars enable quick comparison between customer segments.

### Mistake avoided

Avoided using a pie chart because leadership needs to compare values accurately rather than estimate proportions.

---

## 6. Return Analysis (Bar Chart by Category and Region)

### What question does the chart answer?

Which product categories and regions have the highest return rates?

### Why is the chart type appropriate?

Bar charts allow accurate comparison of return rates across multiple regions within each product category.

### Fields used

* **Columns:** Category
* **X-axis:** Region
* **Y-axis:** Return Rate
* **Color:** Region
* **Filter:** Region

### Design principle applied

Small multiples separate product categories while consistent colors improve regional comparison.

### Mistake avoided

Avoided combining all categories into one crowded chart, which would make regional differences difficult to interpret.

---

# Overall Dashboard Design Principles

* KPI cards are positioned at the top to provide an immediate executive summary.
* Charts are arranged to tell a logical business story: overall performance → sales trend → operational performance → profitability drivers → customer behavior → return risks.
* Consistent fonts, spacing, and color usage improve readability.
* Minimal visual clutter ensures executives focus on business insights rather than decorative elements.
* Appropriate chart types were selected based on the nature of the data (trend, comparison, relationship, or distribution), ensuring accurate interpretation and supporting data-driven decision-making.

