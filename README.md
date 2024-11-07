# HR-LITA-Project
This is where I documented my project done based on my recently acquired knowledge on Data analysis with the Incubator Hub 

# PROJECT TITLE; EMPLOYEE RECORDS AND BEHAVIOURAL PERFORMANCE
---
- [Project Overview](#project-overview)
- [Data Collected](#data-collected)
- [Project Objectives](#project-objectives)
- [KEY metrics](#key-metrics)
- [Tools Used](#tools-used)
- [Data cleaning and Preparation](##data-cleaning-and-preparetion)
- [Exploratory Data Analysis](##exporatory-data-analysis)
- [Visual Inference](##visual-inference)

## PROJECT OVERVIEW
----
This project collects and analyse Employee's records/behavioural performance Data from various regions.
The goal is to generate insight into the behavioural performance of employees over the past year by analysing the various parameters in the data received, we seek to gather enough insight to make reasonable decission. 


## DATA COLLECTED
---
The Data collected includes the following key columns;
- Region; The geographical location of each store
- Product; Items sold
- Order date; the day of the week for each transaction
- Quantity; The number of units sold for each transaction
- Unit Price; The amount for each product
- Revenue; The total monetary value generated from sale.
- Customer Name; Names of customers that patronzse the store
  

  ## PROJECT OBJECTIVES
  ---
  This project was designed to tackle the following analysis goal
  1. Sales per Product; To ascertain the total sales per product and the highest selling product
  2. Sales by Region; To determine the total sales by region
  3. Sales by Month; To work out overall sales for each month
  4. Average Revenue by Region; To calculate the avreage revenue per sales in each region.
  5. Transaction by Region; To figure out the number of units sold across different regions to be able to identify the most active location.
  6. Total Rvenue per product: To determine the product with the highest revenue
  7. Total Purchase Amount By Customer; To find the top 5 customers by the total purchase amount
  8. Percentage of Total Sales by Region; To calculate the percentage of total sales contributed by each region.
  9. Product By Order date; To identify products with no sales in the last quarter.
     
 
     ## KEY METRICS
     ---
     - Total sales; Sum of total sales categorized by
       1. Product
       2. Region
       3. Month
     - Units Sold; Sum of units sold grouped by region
     - Average Revenue; Total revenue for each region to evaluate revenue consistency.
     - Total Purchase by Customer; To check the top 5 customer.  
    

     ## TOOLS USED
     ---
     1. Microsoft Excel [DownloadHere](https://www.microsoft.com)
      - Summarize and format data for easier interpretation using pivot table.
      - Bar Charts were created to visually represent the key findings.
     2. SQL (structured query language) [DownloadHere](https://www.microsoft.com)
      - For querying data. Example:
        1. SELECT Product, SUM(UnitPrice) AS TotalSales
           FROM SalesData
           GROUP BY Product
        2. SELECT Region, COUNT(orderID) AS No_of_Transactions
           FROMSalesData
           GROUP BY Region
        3. SELECT Top (1) Product, SUM(UnitPrice)
           AS TotalSales
           FROM SalesData
           GROUP BY Product
           ORDER BY TotalSales DESC 
        4. SELECT Product, SUM(UnitPrice) AS TotalRevenue
           FROM SalesData
           GROUP BY Product  
        5. SELECT Month(orderDate) AS Month, SUM(UnitPrice) AS MonthlyTotal
           FROM SalesData
           WHERE YEAR(OrderDate) =2024
           GROUP BY Month(OderDate)
           ORDER BY Month
        6. SELECT Top (5) Customeer_id,
           SUM(UnitPrice) AS TotalPurchseAmount
           FROM SalesData
           GROUP BY Customer_id
           ORDER BY TotalPurchaseAmount DESC 
        7. SELECT Product FROM SalesData
           GROUP BY Product
           HAVING SUM(CASE WHEN OrderDate BETWEEN '2024-06-01' AND '2024-08-31' THEN 1 ELSE 0 END) = 0            
     3. Microsoft Power BI [DownloadHere](https://www.microsoft.com)
      - for data cleaning and fomatting
      - To visually represent the key findings
    

     ## DATA CLEANING AND PREPARATION
     ---
     The following actions were performed for the data cleaning and preparation
       1. Data loadind and inspection; Retrieve data from source and indentify missing or inconsistent values
       2. Data cleaning and Formatting; Identify and correct errors, inconsistencies and inaccuracies in the data, transform data into a consistent and suitable format for analysis.


          ## EXPLORATORY DATA ANALYSIS
          ---
          - Sales Per Product; Group data by product and sum of unit price column. This provides an overview of how much sales is realised from each product.
          - Sales by Region; Group data by region and sum of revenue column. To determine how much revenue each region is generating
          - Sales Per Month; Group data by month and sum of unit price column. To identify the period with the highest sales
          - Unit Sold by Region; Group data by region and sum of quantity column. To mearsure the most active region
          - Average Revenue by Region; To get the average revenue per transaction in each region.
         


            ## VISUAL ANALYSIS AND INFERENCE
            ---
