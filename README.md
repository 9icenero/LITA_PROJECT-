# Project Title
---
## Sales Performance Analysis Project


### Table Outline for the Portfolio
---
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools Used](#tools-used)
- [Data Dictionary](#data-dictionary)
- [Data Cleaning and Preparations](#data-cleaningand-preparation)
- [Data Analysis](#data-analysis)
- [Data Visualization](#data-visualization)
- [Conclusion](#conclusion)
- [Recommendation](#recommendation)

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

### Data Dictionary
Outline the terminology and definitions of key column headers specific to the dataset. This section ensures clarity for anyone reviewing the project.

i.  OrderID: A unique number that identifies each order made by a customer.

ii.  Customer ID: A unique number assigned to each customer to keep track of their orders.

iii  Product: The name or type of item that is being sold.

iv  Region: The area or location where the customer is from or where the sale occurs.

v  Order Date: The date when the order was placed.

vi  Quantity: The number of items ordered.

vii  Unit Price: The cost of a single item.

viii  Total Sales: The total money made from an order, calculated by multiplying the quantity by the unit price.

### Data Cleaning and Preparations
----
In the initial phase of the data cleaning and preparations, we preform the following actions;
1.  Data inspection and loading
2.  Handling missing variables
3.  Data cleaning and formatting

### Exploratory data Analysis
----
#### Retail Store Sales 

This analysis focused on answering key business questions, inorder to support strategic decisions in sales performance and customer including:

- Calculating total sales for each product category.
- Determining the number of sales transactions in each region.
- Identifying the highest-selling product based on total sales value.
- Calculating total revenue for each product.
- Summing monthly sales totals for the current year.
- Identifying the top 5 customers by total purchase amount.
- Calculating the percentage contribution of each region to total sales.
- Finding products with no sales in the last quarter.

### Data Analysis
---
```SQL
Retrieve the total sales for each product category.

SELECT Product, SUM(Total_Sales) AS Total_Sales from [dbo].[SalesData]
GROUP BY Product;
<img width="169" alt="image" src="https://github.com/user-attachments/assets/cb24487d-21de-4084-abf6-30fe237156e9">

```
Find the number of sales transactions in each region.
```
Find the highest-selling product by total sales value.

```
Calculate total revenue per product. 

```
Calculate monthly sales totals for the current year.

```
Find the top 5 customers by total purchase amount. 

```
Calculate the percentage of total sales contributed by each region.

```
Identify products with no sales in the last quarter. 

```

### Data Visualization
---


### Conclusion
---


### Recommendation
