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
1. Retrieve the total sales for each product category.

SELECT Product, SUM(Total_Sales) AS Total_Sales from [dbo].[SalesData]
GROUP BY Product;
```
<img width="169" alt="image" src="https://github.com/user-attachments/assets/2e7d1d7f-6276-455f-a1c7-de33e39435ad">

```SQL
2. Find the number of sales transactions in each region.

SELECT Region, Count(Total_Sales) AS NumberofSales_Transaction from [dbo].[SalesData]
GROUP BY Region;
```
<img width="208" alt="image" src="https://github.com/user-attachments/assets/2371e0d4-8c57-466c-b724-40f54f879f5e">

```SQL
3. Find the highest-selling product by total sales value.

select top 1 product, sum(quantity*unitprice) as totalsales
From [dbo].[SalesData]
Group by product
Order by totalsales desc;
```
<img width="109" alt="image" src="https://github.com/user-attachments/assets/2215a688-6bd7-4c9f-af0e-c299a607bd66">

```SQL
4.  Calculate total revenue per product.
   
Select Product, SUM(Total_Sales) AS TotalRevenue
From [dbo].[SalesData]
Group by Product;
```SQL
5.  Calculate monthly sales totals for the current year.

Select Product, SUM(Total_Sales) AS TotalRevenue
From [dbo].[SalesData]
Group by Product;
```
<img width="143" alt="image" src="https://github.com/user-attachments/assets/6b491bb8-bd23-4879-8426-b5894de7297b">

```SQL
6.  Find the top 5 customers by total purchase amount.

Select top 5  Customer_Id, Sum(Total_Sales) AS TotalPurchase
From [dbo].[SalesData]
Group By Customer_Id
Order By TotalPurchase Desc;
```
<img width="146" alt="image" src="https://github.com/user-attachments/assets/f1b382e5-85ad-44c2-8388-7e206ea64512">

```SQL
7.  Calculate the percentage of total sales contributed by each region.

SELECT  region, 
    SUM(quantity * unitprice) AS TotalSales,
    SUM(quantity * unitprice) * 1.0 / (SELECT SUM(quantity * unitprice) FROM [dbo].[SalesData]) * 100 AS PercentageOfTotalSales
FROM 
    [dbo].[SalesData]
GROUP BY 
    region;
```

<img width="208" alt="image" src="https://github.com/user-attachments/assets/63a42990-1174-4934-9bd9-1addc2d964be">

```SQL
8.  Identify products with no sales in the last quarter. 

Select distinct product
From [dbo].[SalesData]
Where product Not In(
Select product
From [dbo].[SalesData]
Where OrderDate >= DateAdd(quarter, -1, GetDate()) and OrderDate < GetDate());
```

<img width="120" alt="image" src="https://github.com/user-attachments/assets/6e683d9b-4879-4922-a905-e296b31f3c5e">


### Data Visualization
---
<img width="488" alt="Screenshot 2024-11-04 224905" src="https://github.com/user-attachments/assets/c5a5e398-63c4-46f4-a88e-c4328c93cce5">

<img width="485" alt="Sales Analysis" src="https://github.com/user-attachments/assets/d4ff5854-d7a8-47b2-81e4-1122c1f65916">



### Conclusion
---


### Recommendation
