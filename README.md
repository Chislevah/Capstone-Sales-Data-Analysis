# Capstone-Sales-Data-Analysis

## Project Topic: Capstone Sales Analysis

### Sales Analysis Project Overview

The Sales Analysis Project is designed to provide a detailed examination of sales data to uncover valuable insights into customer behavior, product performance, and revenue trends. This project integrates Power BI, SQL, and Excel to create a robust framework for analyzing sales performance and identifying actionable business insights.

### Project Goals

- To visualize key sales metrics and trends using Power BI dashboards.
- To utilize SQL for data extraction, manipulation, and advanced analysis.
- To leverage Excel for additional data visualization and analysis, making insights more accessible for various stakeholders.
- To help businesses make data-driven decisions to optimize sales strategies and improve performance.

### Key Components

1. Power BI Sales Dashboard:
   - Purpose: Create interactive and visually compelling dashboards to monitor sales performance.
   - Key Visuals:
     1. Revenue Trend Analysis: Line chart showing monthly or quarterly sales trends.
     2. Top Products by Revenue: Bar chart highlighting the best-selling products.
     3. Regional Sales Performance: Heat map or column chart displaying sales by region.
     4. Sales KPIs: Cards showing total sales, average order value, and top customer segments.
    - Features:
    - Filters and slicers for interactive data exploration (e.g., by product, region, or sales period).
    - Drill-down capabilities to explore sales at different levels (e.g., region to city).
      
2. SQL Queries for Data Analysis:
   - Purpose: Extract and analyze sales data from databases for deeper insights and reporting.
   - Example Queries:
     1. Total Revenue Query: Calculate total sales revenue grouped by product and region.
     2. Customer Analysis Query: Identify top customers based on purchase volume and revenue.
     3. Sales Trend Query: Extract data for trend analysis by month or quarter.
    - SQL Features:
      1. Use of GROUP BY, JOIN, and WHERE clauses for aggregating and filtering data.
      2. Advanced queries using subqueries and window functions for ranking and trend analysis.
            
3. Excel Sales Analysis:
- Purpose: Use Excel to create pivot tables, charts, and summary reports for quick analysis.
- Key Analyses:
  1. Sales by Product: Create pivot tables summarizing revenue by product category.
  2. Sales Growth Analysis: Use Excel charts to visualize revenue growth over time.
  3. Customer Segmentation: Analyze customer purchases and identify high-value segments using Excel functions.
- Excel Features:
  1. Conditional formatting for visual emphasis on key metrics.
  2. Use of formulas such as SUMIFS, AVERAGEIFS, and VLOOKUP for customized calculations.

     
### Insights and Analysis Goals

1. Sales Trends: Identify periods of peak sales activity and seasonal patterns.
2. Top Performing Products: Recognize which products drive the most revenue.
3. Regional Insights: Analyze which regions contribute the most to total sales and identify growth opportunities.
4. Customer Insights: Determine the characteristics of high-value customers and average order value.
5. Revenue Growth: Track revenue growth over time and identify periods with significant changes.
   
### Importance of this Analysis

1. Sales Strategy Optimization: Use insights from the analysis to refine product offerings, pricing strategies, and marketing efforts.
2. Performance Tracking: Monitor key sales performance indicators to ensure targets are being met.
3. Resource Allocation: Identify high-performing regions or products to allocate resources effectively.
4. Customer Relationship Management: Develop targeted campaigns based on customer buying behavior and preferences.

### Intended Audience

1. Sales Managers who need to track sales performance and identify areas for growth.
2. Data Analysts looking for examples of integrating Power BI, SQL, and Excel for comprehensive analysis.
3. Business Strategists who require a data-driven approach to optimize sales operations.
4. Students and Learners interested in developing sales analysis skills and understanding business intelligence techniques.

### Benefits of the Project

1. Reporting: Combines the visual power of Power BI, the query capabilities of SQL, and the versatility of Excel.
2. Interactive Analysis: Users can explore data through interactive Power BI dashboards.
3. Detailed Documentation: Clear explanations and guides on how the analyses were created and how to replicate them.
4. Actionable Insights: Provides data-driven insights that can influence business decisions and improve sales outcomes.
5. This project serves as a complete example of how to use business intelligence tools to perform a thorough sales analysis and turn raw data into actionable insights.

### Additional Analysis Ideas

- Revenue Trends by Seasonality: Use time intelligence functions in DAX to create year-over-year and month-over-month comparisons.
- Customer Segmentation: Analyze customers by total revenue contributed to understand high-value vs. low-value customers.
- Sales Forecasting: Use built-in forecasting tools in Power BI to project future revenue based on historical data.

#### Microsoft Excel Analysis

To analyze my dataset in Excel, I ran various analyses. I began by creating some new columns which are the total revenue column and the transaction category column.

Total Revenue
```excel
= quantity *unit price

```
Transaction category: created using conditionals formatting for my total revenue. Ranging from 1-150(low), 151-350(medium), >350(high).
```excel
=IF(Revenue<=150,"low",IF(Revenue<=350,"medium","high")).
```
 
Since I was working on a voluminous data I used the auto fill to calculate for the remaining rows of data. Secondly I ran some analysis to calculate average, total sales, total revenue, highest and lowest sales, average order value, total sales by the various products and total sales by region. Here are some key points from my analyses:

a.	Total sales: calculate the total revenue for all orders.
```excel
= SUM(Total Revenue).
```
b.	Average sales: calculate the average revenue for all orders. 
```excel
=AVG(Total Revenue).
```
c.	Highest sale: calculate the highest revenue for all orders. 
```excel
=MAX( Total Revenue).
```
d.	Lowest sales: calculate the lowest sales for all orders 
```excel
=MIN(Total Revenue).
```
e.	Total no of order: 
```excel
=COUNT(order id)
```
f.	Total product sold:
```excel
= SUM(Quantity)
```
g.	Average order value: 
```excel
=SUM(Total Revenue)/ COUNTA(Quantity)
```
h.	Total Socks sold:
```excel
=SUMIF(Products, Socks, Quantity).
```
 This formula I used for all the products sold, I only made changes to the criteria in order to suit each category of products.
 
i.	Sales by region: 
```excel
=SUMIF(Region, west, Total Revenue)
```
 Formula applicable to all sales by various region with changes made on the criteria alone.

Pivot Table Presentation (insert a new sheet for pivot table presentation)

- Revenue by Region: Use a Pivot Select your data range, go to Insert > Pivot Table. Drag Region to the "Rows" area and Total Revenue to the "Values" area. This will give you the total sales for each region.
- Revenue by Product: In the Pivot Table, drag Product to the "Rows" area and Total Revenue to the "Values" area. This will show you total revenue for each product.
- Revenue by Customer: Drag Customer ID to the "Rows" area and Total Revenue to the "Values" area in a Pivot Table. Sort the data to see the customers who generated the highest revenue.
-	Order Count Over Time: Insert a Pivot Table with Month (or Year) in the "Rows" area and Order ID in the "Values" area. This will show you order trends over time.
- 	Top Products Analysis: To find the top-selling products (by revenue or quantity), use a Pivot Table with Product in the "Rows" area and Quantity or Total Revenue in the "Values" area. Sort by Total Revenue or Quantity to find the top products.
-	Regional Sales Comparison: Create a Pivot Table with Region in the "Rows" area and Total Revenue in the "Values" area.
-	Average Order Value (AOV): To find AOV by Region or Product, use a Pivot Table: Insert Region (or Product) into the "Rows" area and Total Revenue into the "Values" area. Change the calculation for Total Revenue to Average by clicking on the field in the Pivot Table, selecting Value Field Settings, and choosing Average.
-	Order Quantity Analysis: To analyze the number of orders made in different regions or for different products. Insert a Pivot Table. Place Region or Product in the "Rows" area and Order ID in the "Values" area, set to Count. This will count the number of orders for each category.
-	Customer Segmentation Use a Pivot Table with Customer ID in the "Rows" area and Total Revenue in the "Values" area.
-	Customer Lifetime Value: If you have a recurring customer base, you can calculate Customer Lifetime Value by summing the total revenue for each customer. Use a Pivot Table with Customer ID in the "Rows" area and Total Revenue in the "Values" area. This will give you the total value each customer has brought in.
-	Product Performance Over Time: To see how different products perform over time: Create a Pivot Table. Place Product in the "Rows" area, Order Date (grouped by month/quarter) in the "Columns" area, and Total Revenue in the "Values" area. This shows how sales of each product vary over time.
-	Repeat Customer Analysis: Check how many customers made more than one order by counting orders for each Customer ID.
-	Profit per Region/Product/Customer: Use calculated fields in your Pivot Table to analyze profit based on different groupings.

Dash Board analysis/ presentation
1. On your insert tab, under shapes select the rectangle.
2. .	Draw out the shape.
3. 	Go to format and select the shape fill from the shape style to edit and format it.
4. 	 Type the name of the report you want to create and edit it from the home table.
5. Select the pivot table you want to create a chart with using ctrl A.
6. Press alt F1.
7. 	Select the chat and press ctrl X.
8. 	 Go to your dashboard and paste your chart using ctrl V.
9.   Right click on any of the field buttons and select hide all field buttons.
10.	To remove the grade lines on your chart select any of the grade lines, click on it and press delete on your keyboard.
11.	The total on the chart box is called your legend and it can be removed by selecting it and deleting it.
12.	Rename the total on the screen to the description of the chart.
13.	To design your chart click on it and select change chart type from the options.










