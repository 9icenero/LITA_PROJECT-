### Project Title
---
** Sales Performance Analysis Project**


### Table Outline for the Portfolio
---
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools Used](#tools-used)
- [Data Cleaning and Preparations](#data-cleaningand-preparation)
- [Data Analysis](#data-analysis)
- [Data Visualization](#data-visualization)
- [Conclusion](#conclusion)
- [Recommedndation](#recommendation)

### Project Overview
---
This project involves a comprehensive analysis of a retail store sales data to evaluate product performance, pinpoint top-selling items/product, and comparing monthly sales across various regions from 2023 to 2024. The primary aim is to uncover trends and patterns that reveal insights into customer preferences and regional variations in sales. By identifying the best-performing products and understanding sales dynamics, this analysis will provide valuable data-driven insights to support informed business decisions, optimize product offerings, and enhance customer retention strategies. Ultimately, the findings will serve as a foundation for improving sales performance and driving growth in targeted areas in the upcoming years.

### Data Sources
---
The primary source of data used here is Lita Capstone Dataset.CSV. This will be made available for view.

### Tools Used
---
- Microsoft Excel [Lita Capstone Dataset Download](https://shorturl.at/iVtt2)
  1. For data cleaning
  2. For Analysis
     
- SQL - Structured Query Language for Querying of Data
- Power B.I - For visualization of the dataset
- GitHub for Portfolio Building

### Data Cleaning and Preparations
----
In the initial phase of the data cleaning and preparations, we preform the following actions;
1.  Data inspection and loading
2.  Handling missing variables
3.  Data cleaning and formatting

### Exploratory data Analysis
----
#### Retail Store Sales 
This involved analysing the data to answer the following questions;
- Retrieve the total sales for each product category. 
- Find the number of sales transactions in each region. 
- Find the highest-selling product by total sales value. 
- Ccalculate total revenue per product. 
- Calculate monthly sales totals for the current year. 
- Find the top 5 customers by total purchase amount. 
- Calculate the percentage of total sales contributed by each region. 
- Identify products with no sales in the last quarter. 

### Data Analysis
---
```SQL
Select top 5  Customer_Id, Sum(Total_Sales) AS TotalPurchase
From [dbo].[SalesData Table]
Group By Customer_Id
Order By TotalPurchase Desc;

```
Select Product, SUM(Total_Sales) AS TotalRevenue
From [dbo].[SalesData Table]
Group by Product;

### Data Visualization
---


### Conclusion
---


### Recommendation
