1-Data Collection
Source: Raw sales data exported from Amazon Seller Central or sample dataset (CSV/Excel).
Data contains: Order ID, Product, Category, Customer, Region, Market, Sales, Returns, and Profit.

2-Data Cleaning (Power Query)
Removed duplicates, null values, and canceled orders.
Standardized date format and ensured correct data types.
Fixed inconsistencies (e.g., merged similar product names, unified regions/markets).
Calculated additional columns: Returns, Profit, KPI metrics.

3-Data Modeling
Built a star schema with Fact table (Orders/Sales) and Dimension tables (Date, Customer, Product, Region, Segment).
Relationships created between fact and dimension tables.

4-DAX Calculations
Total Sales = SUM(Sales[SalesAmount])
Profit = SUM(Sales[Profit])
Return = COUNTROWS(FILTER(Sales, Sales[Status]="Returned"))
KPI measures (Units Sold, Top/Bottom Products, Profit by Segment).

5-Dashboard Creation (Power BI)
Cards/KPIs: Show quick metrics → Sales Projection, Product Units, KPI, Returns.
Pie/Donut Charts: Sales by Segment and Sales by Market → best for showing proportion/distribution.
Map Visualization: Sales by Region → highlights geographical spread of sales.
Bar Chart (Customer Profit): Easy comparison of top customers by profit.
Horizontal Bar Charts: Bottom 5 & Top 5 Profit Products → clear ranking visualization.

6-Formatting & Storytelling
Consistent color theme (orange + blue).
Added slicers (Year filter: 2012–2015) for time analysis.
Used tooltips and labels for clarity.

7-Publishing & Sharing
Published to Power BI Service.
Setup scheduled refresh to keep data updated.
Shared report with stakeholders via link.


## Why Different Charts Are Used?

Cards: Show key KPIs at a glance (Sales, Units, Returns).

Pie/Donut Charts: Good for showing share of sales by category/market.

Map: Perfect for geographical insights.

Bar Charts: Great for ranking customers/products by profit.

Comparison Charts (Top 5 / Bottom 5): Quickly identify best and worst performers.

## Tools Used

Microsoft Excel → Initial data cleaning and export.
Power BI (Power Query + DAX) → Data transformation, modeling, dashboard creation.
Power BI Service → Online publishing, refresh scheduling, sharing.
