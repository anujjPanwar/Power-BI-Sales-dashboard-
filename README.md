# Power-BI-Sales-dashboard

![GitHub Logo](https://github.com/anujjPanwar/Power-BI-Sales-dashboard-/blob/main/Screenshot%20Dashboard%202017%20-%202019.png)

# Objective
Our objective is to streamline the process of data collection, preparation, and cleaning to ensure the accuracy and consistency of our dataset. Subsequently, we aim to leverage data modeling techniques to establish meaningful relationships between various data sources, laying a robust foundation for our analysis.

As we progress, our focus will shift to harnessing the capabilities of Power BI Desktop to create visually compelling reports that effectively communicate key metrics and trends. Through intuitive visualizations and interactive features, we'll craft charts, graphs, and tables that offer valuable insights into our business operations.

Moreover, we'll delve into advanced techniques such as implementing DAX calculations, building dynamic filters and slicers, and leveraging collaboration and sharing features within Power BI.

By the conclusion of this project, our goal is to deliver a comprehensive Power BI Sales Dashboard that empowers our organization to make informed, data-driven decisions, optimize sales strategies, and ultimately drive business growth and success.


[Click here to access the Power BI Service](https://app.powerbi.com/groups/me/reports/88309439-22fc-409a-9383-b429db5c0061/ReportSectionf284c540955942f08571?experience=power-bi&clientSideAuth=0)




#### Table of Contents
The Objective of the Sales Dashboard / Business Problem
Steps to follow for an end-to-end Power BI Project
1) Gather Data
2) Power Querry – Data Extract, Transform & Load
3) Create a Date Table
4) Create Data Model in Power BI Desktop
5) Develop Reports in Power BI Desktop
6) Implementing DAX Calculations
Conclusion of Power BI Sales Dashboard Project
Download Power BI Project PBIX File & Excel Dataset

## The Objective of the Sales Dashboard / Business Problem
The objective of the report is to analyze and present comprehensive insights into sales, profit, orders, profit margin, and various comparisons. It aims to provide a clear understanding of key performance indicators and trends using Power BI. The report objectives can be summarized as follows:

#### Calculate Profit: 
Calculate and visualize the total profit achieved based on the sales data, providing insights into the financial performance.
#### Analyze Orders: 
Analyze the number of orders placed during the selected period, helping to identify sales patterns and order trends.
#### Calculate Profit Margin: 
Calculate and visualize the profit margin percentage, enabling users to assess the profitability of products or services.
#### Compare Sales by Product with Previous Year: 
Compare sales performance for each product between the selected period and the previous year, highlighting growth or decline in sales.
#### Compare Sales by Months with Previous Year: 
Compare sales performance across different months between the selected period and the previous year, identifying regions with significant changes.
#### Display Top 5 Cities: 
Present a visualization showcasing the top 5 cities based on sales, allowing users to quickly identify the most lucrative locations.

# Steps to follow for an end-to-end Power BI Project
## 1. Gather Data

- Collect relevant data from various sources such as databases, spreadsheets, or web services.
- Ensure data accuracy and relevance to the project objective.

## 2. Power Query – Data Extract, Transform & Load (ETL)

- Utilize Power Query Editor in Power BI for data cleaning and transformation.
- Perform tasks such as removing duplicates, handling missing values, merging datasets, or creating calculated columns.

## 3. Create a Date Table

- Create a date table to facilitate the use of Data Analysis Expressions (DAX) time intelligence functions.
- Ensure to turn off Auto Date/Time for new files in Power BI Options Setting to improve report performance.

## 4. Create Data Model in Power BI Desktop

- Design and create a data model representing relationships between different tables.
- Establish proper relationships, define keys, and hierarchies if needed for accurate analysis and visualization.

## 5. Develop Reports in Power BI Desktop

- Use Power BI Desktop to create reports based on the data model.
- Add visualizations such as charts, tables, and maps to effectively represent the data.
- Apply filters, slicers, and drill-through functionalities for interactive user experience.

### Report Background in PowerPoint

- Create background visuals in PowerPoint.
- Create slicers for Date, City, Product, and Channel.
- Define DAX measures.
- Create visuals for:
  1. Sales By Product and Comparison with last year’s Sales.
  2. Sales By Month and Comparison with last year’s Sales.
  3. Sales of top 5 Cities.
  4. Compare Profit by channel with Previous year’s Profit.
  5. Sales By Customer and Comparison with last year’s Sales.
  6. Create Cards for Sales, Profit, Profit Margin & Product Sold.

#### Sales By Product and Comparison with last year’s Sales.

![GitHub Logo](https://github.com/anujjPanwar/Power-BI-Sales-dashboard-/blob/main/Screenshot%20Sales%20and%20sales%20PY%20by%20Product%20Name.png)

#### Sales By Month and Comparison with last year’s Sales.

![GitHub Logo](https://github.com/anujjPanwar/Power-BI-Sales-dashboard-/blob/main/Screenshot%20Sales%20and%20Sales%20PY%20by%20Monthly.png)


#### Compare Profit by Channel with Previous Year: 
Compare profit generated by each channel between the selected period and the previous year, indicating improvements or challenges in profitability.

![GitHub Logo](https://github.com/anujjPanwar/Power-BI-Sales-dashboard-/blob/main/image%20of%20sales%20of%20comprasion%20with%20pre.%20by%20channel.png)


#### Analyze Sales by Customer and Compare with Previous Year: 
Analyze sales data by customer, highlighting the performance of individual customers and comparing it to the previous year.

![GitHub Logo](https://github.com/anujjPanwar/Power-BI-Sales-dashboard-/blob/main/Screenshot%20Sales%20and%20sales%20PY%20by%20Channel%20Names.png)

#### Create Slicers for Date, City, Product, and Channel: 
Enable users to interact with the data by providing slicers for selecting specific dates, cities, products, and channels, allowing for dynamic filtering and personalized analysis.

## 6. Implementing DAX Calculations
- Use Data Analysis Expressions (DAX) to create calculated columns, measures, and tables for complex calculations and aggregations.

// Measures Total Sales
Sales = SUM(Sales_Data[Sales])

// Measures Previous Year Total Sales
Sales PY = CALCULATE([Sales], SAMEPERIODLASTYEAR(DateTable[Date]))

// Difference Between Current Year Sales & Previous Year Sales
Sales vs PY = [Sales] - [Sales PY]

// Percentage Increase or Decrease in sales year on year (YOY%)
Sales vs PY % = DIVIDE([Sales vs PY],[Sales],0)

// Products Sold
Products Sold = SUM(Sales_Data[Order Quantity])

// Profit
Profit = SUM(Sales_Data[Profit]) 

// Profit Last Year
Profit LY = CALCULATE([Profit], SAMEPERIODLASTYEAR(DateTable[Date]))

// Profit Vs Last Year
Profit Vs LY = [Profit] - [Profit LY]

// Profit vs Last Year Percentage
Profit vs LY % = [Profit Vs LY] / [Profit]

// Profit Margin
Profit Margin = DIVIDE([Profit],[Sales],0)

// Total Cost
Total Cost = SUM(Sales_Data[Total Cost]) 


# Conclusion of Power BI Sales Dashboard Project

### Year 2019 Analysis:

1. **Sales Decline:**
   - Sales experienced a significant decrease of more than 10% compared to the previous year.

2. **Product Sales Decline:**
   - All the top 7 products exhibited a drop in sales, indicating a broad decline across product lines.

3. **Customer Impact:**
   - Analysis revealed that sales were adversely affected by the behavior of 4 specific customers, contributing to the overall sales decline.

4. **Profit Margin Insight:**
   - Notably, the Export channel demonstrated a higher profit margin compared to other sales channels, presenting opportunities for further exploration and potentially focusing sales efforts.

### Recommendations:
Based on the conclusions drawn from the analysis, the following recommendations are suggested:

1. **Targeted Customer Engagement:**
   - Implement targeted strategies to address the concerns or behaviors of the identified customers impacting sales negatively.

2. **Product Portfolio Evaluation:**
   - Conduct a thorough evaluation of the product portfolio to identify opportunities for innovation, improvement, or marketing efforts to stimulate sales growth.

3. **Channel Optimization:**
   - Explore opportunities to leverage the higher profit margin observed in the Export channel by optimizing resources and strategies in alignment with market demand.

By addressing these key insights and implementing strategic recommendations, the organization can mitigate the challenges identified in the analysis and drive future sales growth and profitability.


