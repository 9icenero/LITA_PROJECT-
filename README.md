### Project Title
---
**Customer & Sales Performance Analysis Project**


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
This project focuses on analyzing two main areas:
1. Retail Store Sales: The aim of the analysis is to check the performance of various products, to determine the bestsellers, and to compare the different region sales in different months from 2023 to 2024..
The goal is to find patterns and insights to help improve our business decisions on sales and customer retention.

2. Customer Subscriptions: Looking at trends on how customers subscribe, cancel, and renew. Also to identify the most popular subscription type.

### Data Sources
---
The primary source of data used here is Lita Capstone Dataset.CSV. This will be made available for view.

### Tools Used
---
- Microsoft Excel [Download Here](http://mxj6.2.vu/2)
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
a. retrieve the total sales for each product category. 
b. find the number of sales transactions in each region. 
c. find the highest-selling product by total sales value. 
d. calculate total revenue per product. 
f. calculate monthly sales totals for the current year. 
g. find the top 5 customers by total purchase amount. 
h. calculate the percentage of total sales contributed by each region. 
i. identify products with no sales in the last quarter. 

#### Customer Subscriptions
 This involved analysing the data to answer the following questions;
a. retrieve the total number of customers from each region. 
b. find the most popular subscription type by the number of customers. 
c. find customers who canceled their subscription within 6 months. 
d. calculate the average subscription duration for all customers. 
e. find customers with subscriptions longer than 12 months. 
f. calculate total revenue by subscription type. 
g. find the top 3 regions by subscription cancellations. 
h. find the total number of active and canceled subscriptions. 

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
