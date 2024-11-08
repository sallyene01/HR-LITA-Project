# HR-LITA-Project
This is where I documented my project done based on my recently acquired knowledge on Data analysis with the Incubator Hub 

# PROJECT TITLE; EMPLOYEE RECORDS AND BEHAVIOURAL PERFORMANCE
---
- [Project Overview](#project-overview)
- [Data Collected](#data-collected)
- [Project Objectives](#project-objectives)
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
- States; The geographical location of each store.
- Attrition; Current and ex employees.
- Age; Age of Employees. 
- Educational Field; Field of study of Employees.
- Job Role; Role of Employees.
- Gender; The Gender of Employees.
- Marital Status; Marital Status of Employees.
- Department; The department of employees.
- Performance Rate; The Rating of Employees' performance.
- Job satisfaction; The level of satisfaction of each employee.
- Hourly Rate;
- Daily Rate;
- Momthly Rate;
- Monthly Income;
  
  

  ## PROJECT OBJECTIVES
  ---
  This project was designed to tackle the following analysis goal
  1. State; The geograhpical location by longitude and latitude.
  2. Attrition; Attrition Count by
     1. Age band
     2. Job role
     3. Educational field
     4. Gender
     5. Marital Status
     6. Department
  3. Performance Rate; Performance Rate by
     1. Job Role
     2. Marital Status
     3. Gender
     4. Educational field 
  4. Job Satisfaction; Job Satisfaction by
      1. Educational Field
      2. Job Role
      3. Gender
      4. Marital Status 
  5. Monthly Income; Total monthly income
  6. Monthly Rate; Average Monthly rate
  7. Daily Rate; Percentage of Daily Rate
  8. Hourly Rate; 
    

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
