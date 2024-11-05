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
  

<img width="314" alt="Screenshot 2024-11-05 135334" src="https://github.com/user-attachments/assets/29b75d79-5882-4358-8cba-248d3dba27d0">

<img width="405" alt="Screenshot 2024-11-05 135308" src="https://github.com/user-attachments/assets/87e922fb-00d0-409e-93cb-c8a7d177ec16">

<img width="960" alt="Screenshot 2024-11-05 135520" src="https://github.com/user-attachments/assets/f305c634-5f5a-476a-ac9a-35ef5481517b">

<img width="892" alt="Screenshot 2024-11-05 135420" src="https://github.com/user-attachments/assets/0c5a2f01-019a-4910-bc28-9ca64b3e4753">

<img width="746" alt="Screenshot 2024-11-05 135737" src="https://github.com/user-attachments/assets/14bcd868-88a4-4269-a218-fff5390bead8">

<img width="933" alt="Screenshot 2024-11-05 135701" src="https://github.com/user-attachments/assets/7c159780-4900-478d-9e66-70567bec8b5f">


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

Excel visualization on my dashboard

- Create a Line Chart to visualize sales trend over time.
- Using a Bar Chart  visualize sales by region, revenue by products.
- Using a pie chart visualize order by quantity.

#### SQL Data Analysis Report and Presentataion
The idea was to create a fresh data base for my project, but then I changed my mind against it since we already had a database solely for anything that involved the incubator hub LITA. I then selected a new query since I was going to be running a fresh analysis on a fresh set of data. The next phase was to import my data into my SQL server. To do this I had to convert my excel file into a CSV format (command delimited) to convert the excel workbook into a CSV format is easy. 
1.	Go to your file on excel,
2.	 Select save as 
3.	Change the file name if necessary
4.	Select the drop down on save as type, choose the CSV format (command delimited)
5.	Select ok
6.	Say yes and ok to whatever question box may appear, but make sure you the instructions properly to understand what is required of you.
7.	Close the file.
   
Now the steps involved in importing my file into my database are as follows;
- 	Right click on the database (LITA_DB).
- 	Navigate to task
- 	Select import flat files( for a CSV file) an argument box would appear
- 	 Click on next
-   Click on browse and navigate to the file you want to open
- Change the table name (optional), next
- 	Review data, next
- 	 Modify column, next
- 	 Summary, next
- Finish, close.
- 	 Refresh database
- Expand table
- 	Run query
- 	 Results.

After importing my sales data into my database, the first query I ran was to be able to see the results of my newly imported table. 
```sql
Select * from [dbo].[LITA Capstone Dataset SALES DATA SET]
```
This showed me my table with the following fields; order_id, customer_id, products, region, order_date, quantity, unit_price, total_revenue. I got a total of 50,000 records. I spent time cleaning my data on Sql to prepare it for further analysis.

Below is the SQL Server-compatible version of each query used in this analysis:
1. Retrieve the total sales for each product category: Since the dataset has no explicit product category, products represents different categories:
```sql
Select products, count(Total_Revenue) as numb_of_sales from [dbo].[LITA Capstone Dataset SALES DATA SET] group by Products
```
2. Find the number of sales transactions in each region: This query will count the number of distinct orderids in each region:
```sql
Select region, count(Total_Revenue) number_of_sales_transactions_in_each_region from [dbo].[LITA Capstone Dataset SALES DATA SET] group by Region
```
3. Highest-selling product by total sales value: To find the product with the highest total sales, sum the totalrevenue for each product and sort:
```sql
Select Products, sum(Total_Revenue) as total_sales from [dbo].[LITA Capstone Dataset SALES DATA SET] group by Products order by 1 desc
```
4.	 Calculate total revenue per product: This query calculates the total revenue for each product:
```sql
Select Products, sum(Total_Revenue) as total_revenue_per_product from [dbo].[LITA Capstone Dataset SALES DATA SET] group by Products
```
5. Calculate monthly sales totals for the current year: To calculate monthly sales, you can extract the month and year from the orderdate and filter for the current year:
```sql
select YEAR(orderdate) as year, MONTH(orderdate) as month,SUM(total_revenue) as total_sales from [dbo].[LITA Capstone Dataset SALES DATA SET] where YEAR(OrderDate) =2024 group by YEAR(OrderDate),MONTH(OrderDate) order by year, month
```
6.	Find the top 5 customers by total purchase amount: To find the top customers by total purchase value:
```sql
select top 5 Customer_Id,  SUM(Total_Revenue) as total_purchase_amt from [dbo].[LITA Capstone Dataset SALES DATA SET] group by Customer_Id order by total_purchase_amt desc
```
7.  Calculate the percentage of total sales contributed by each region: This query calculates the percentage of sales per region compared to the total sales:
```sql
WITH total_sales as( select SUM(total_revenue) as sumofrevenue from [dbo].[LITA Capstone Dataset SALES DATA SET]) Select region, SUM(total_revenue) as totalrevenue, (SUM (total_revenue) * 100.0 / (select sumofrevenue from total_sales)) as percentage_of_total_sales from [dbo].[LITA Capstone Dataset SALES DATA SET] group by region
```
8.  Identify products with no sales in the last quarter: To find products with no sales in the last quarter, you need to compare the orderdate with the current quarter:
```sql
SELECT count(Total_Revenue) as total_sales_in_last_quarter, Products FROM  [dbo].[LITA Capstone Dataset SALES DATA SET] WHERE DATEPART(QUARTER, orderdate)=3 and YEAR(OrderDate)= 2024 GROUP BY Products.
```

Some further analysis were also carried out as can be seen in the actual work and my screenshots

<img width="542" alt="Screenshot 2024-11-05 140607" src="https://github.com/user-attachments/assets/77d6696c-89da-469d-b66d-7aaf80a67e26">

<img width="960" alt="Screenshot 2024-11-05 140210" src="https://github.com/user-attachments/assets/49727dd9-404d-4875-87cc-f8cdb1e65b10">

<img width="474" alt="Screenshot 2024-11-05 140523" src="https://github.com/user-attachments/assets/fa468cec-d594-47ba-939c-24252ac8de6c">

<img width="960" alt="Screenshot 2024-11-05 140409" src="https://github.com/user-attachments/assets/27bb3a20-e6ba-4d47-a9cb-6b011ffd3a01">

<img width="960" alt="Screenshot 2024-11-05 140302" src="https://github.com/user-attachments/assets/4b7a3f77-5b8a-4ed6-ae45-53a7c4f789b0">


#### Power BI Analysis Report

To effectively analyze the dataset in Power BI, you can create various calculations and visualizations to gain insights into sales and customer behavior. Below, I provide a more detailed explanation of the types of analyses, metrics, and visualizations you could use, as well as their business implications after I had imported transformed and loaded my data. 

Comprehensive Calculations and Measures:
- Revenue: This column helps you understand the total income generated from sales. It’s critical for assessing overall business health.
 ```DAX
Revenue= SalesData[Quantity] * SalesData[Unit Price]
```
-  Total Quantity:
```DAX
Total Quantity = SUM(SalesData[Quantity])
```
- Total Revenue:
```DAX
Total Revenue= SUM(SalesData[Revenue]
```
- Average Revenue per Order: This KPI is useful for understanding the typical revenue generated from each transaction. It’s a strong indicator of sales efficiency and helps in assessing whether high volumes correlate with high revenue or if the business relies on larger orders.
```DAX
Order = AVERAGEX(SalesData, SalesData[Total Revenue])
```
- Number of Unique Customers: Tracking this metric helps gauge market penetration and customer base growth. A growing number of unique customers indicates successful acquisition strategies, while stagnation may suggest the need for new marketing efforts.
```DAX
Unique Customers =DISTINCTCOUNT(SalesData[Customer ID])
```
- Revenue Growth Percentage: This measure is vital for comparing performance across time periods (e.g., year-over-year, month-over-month). It helps identify trends, showing if the business is growing, stable, or declining.
```DAX
Revenue Growth % = DIVIDE( [Total Revenue] - CALCULATE([Total Revenue], PREVIOUSMONTH(SalesData[Order Date])), CALCULATE([Total Revenue]), PREVIOUSMONTH(SalesData[Order Date])), 0).
```
OR
```DAX
YoY Revenue Change = DIVIDE( [Total Revenue] - CALCULATE([Total Revenue], SAMEPERIODLASTYEAR(SalesData[Order Date])), CALCULATE([Total Revenue], SAMEPERIODLASTYEAR(SalesData[Order Date])), 0)
```
•	Revenue by Region :
```DAX
= SUMX(FILTER(SalesData, D[Region] = "Region Name"), SalesData[Total Revenue]).
```
•	Total Orders:
```DAX
Total Orders= DISTINCTCOUNT(SalesData[Orderid])
```

Visualizations

1. Bar Chart/Column Chart:
   - Total Revenue by Product: Shows which products generate the most revenue.
   - Total Revenue by Region: Highlights the best-performing regions.
   - Quantity Sold by Product: Shows which products are sold most frequently.
     
2. Line Chart:
   -  Revenue over Time: Illustrates trends and seasonality in revenue over time (e.g., monthly or quarterly).
   -  Revenue Growth Rate: Displays growth trends to see performance improvement or decline.
   - 
3. Pie Chart/Donut Chart:
   -  Revenue Share by Region: Visualizes the percentage contribution of each region to the total revenue.
   -  Product Distribution: Highlights the share of different products in the overall sales.
   - 
4. Table or Matrix:
   - Detailed Sales Report: Displays Orderid, Customer ID, Product, Quantity, Unit Price, and Total Revenue with filters by Region or Order Date.
   - Top 10 Customers by Revenue: A ranked table showing your most valuable customers.

5. Scatter Plot:
   - Revenue vs. Quantity by Product: Assesses the relationship between the quantity sold and the total revenue for different products.
   - 
6. Map Visualization:
   - Revenue by Region: Uses geographical data to show sales distribution visually on a map.

7. Slicer:
   - Create slicers for Order Date, Product, Region, or Customer ID to allow users to filter and interact with the visualizations dynamically.
  
   

Key Visualizations and Their Purpose

1. Bar/Column Charts:
   - Revenue by Product: Quickly identify which products drive the most revenue and make data-driven decisions about product focus.
   - Revenue by Region: Highlights which geographic areas are performing well. This can be crucial for planning regional marketing campaigns or identifying potential areas for expansion.
   - 
2. Line Charts:
   - Revenue Over Time: Visualizing revenue as a time series helps spot seasonality or recurring trends (e.g., peak sales during holidays). Adding trendlines can highlight overall growth or decline.
   - Revenue Growth Rate: This line chart can compare multiple periods, allowing you to assess the consistency of growth and recognize potential periods of stagnation or decline.
     
3. Pie/Donut Charts:
   - Revenue Share by Region: Provides a snapshot of how different regions contribute to total sales, aiding in resource allocation.
   - Product Distribution: Useful for visualizing the diversity of the product catalog's contribution to total revenue.
     
4. Table/Matrix Visualizations:
   - Detailed Sales Report: This visualization acts as a detailed breakdown of sales, enabling deeper insights when filtering by Customer ID, Region, or Order Date.
   - Top 10 Customers by Revenue: This ranked list shows which customers generate the most revenue, which is helpful for targeted marketing or VIP customer engagement.

5. Scatter Plot:
   - Revenue vs. Quantity by Product: This visualization helps identify products with high revenue but low sales volume or vice versa. It’s ideal for understanding product positioning and pricing strategies.

6. Map Visualization:
   - Revenue by Region: An interactive map is useful for showing sales performance across different geographic areas. Users can visually identify strong and weak regions for strategic insights.

7. KPI Indicators: These indicators can be used to show metrics such as total revenue, total orders, and average revenue per customer at a glance, providing quick, actionable insights.

 
Interactive Dashboard Elements
- Slicers: Implement slicers for Order Date, Product, Region, and Customer ID to allow users to interact with the dashboard dynamically. Slicers make it easy to filter data and focus on specific segments or timeframes.

- Drill-Throughs: Enable drill-through functionality so users can click on a specific region or product in a visualization and see detailed data related to that selection. For example, clicking on a region in a map visualization could take you to a detailed sales report for that region.

- Storytelling with Data
Narrative Insights: Use Power BI’s smart narrative feature to generate textual summaries that explain trends and changes in data automatically. This helps stakeholders quickly understand key takeaways without needing to interpret graphs and charts on their own.

- Dashboards for Different Stakeholders: Tailor dashboards for different users (e.g., senior management, sales teams, and marketing departments). For instance, senior management might want high-level KPIs and trends, while sales teams need detailed customer and product performance data.

Actual Visualizations

<img width="960" alt="Screenshot 2024-11-05 141039" src="https://github.com/user-attachments/assets/da1fda14-9de4-4b60-af7d-787e6d3b18bf">

<img width="960" alt="Screenshot 2024-11-05 140738" src="https://github.com/user-attachments/assets/5ef4b1cc-f102-4479-be5b-362c797b7be6">

<img width="960" alt="Screenshot 2024-11-05 140647" src="https://github.com/user-attachments/assets/d2617baf-51d6-42d6-8ef1-ea96ec6e0bff">


