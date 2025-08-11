# AdventureWorks-Production-and-Inventory-Analysis
 
## Overview

This analysis goes through the Production and Inventory Analysis of the Microsoft AdventureWorks Database. Adventure Works is a fictional bicycle manufacturing company, this database contains standard transactions data from an Enterprise Resource Planning System. It contains data from the following scenarios of the company: Human Resources, Product Management, Manufacturing, Purchasing, Inventory, Sales, and Admin. 

This analysis focuses on the Manufacturing and Inventory part of the data. Microsoft Power BI has been used to create an interactive dashboard while pulling data from SQL Server.

## Data Source

[Data Source](https://docs.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver15&tabs=ssms)

## Data Model

<img width="620" alt="DataModel" src="/Demo/Data Model.png">


## Built With

•[Power BI](https://powerbi.microsoft.com/en-us/)
•[SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)

## Detailed Analysis

### Tables used in the model: -

- Production Location - Has Production assembly data, 1.e. Parts used to manufacture each product are defined here with an assembly location category
- Production Product - Data related to products, their physical details, price, etc.
- Production ProductCategory - Products and their defined categories
- Production ProductSubcategory - Products and their subcategories
- Production ProductInventory - Inventory data of the produced products
- Production ScrapReason - Waste Data related to manufacturing
- Production WorkOrder - Production transactions and related data
- Production WorkOrderRouting - Production work order scheduling data and details
- Sales SalesOrderDetail - Transactional Sales Data

## Analysis

This dashboard analyses manufacturing and inventory operations, the dashboard is made to have an app-like navigational interface. The main page includes leads to two areas namely Production Overview and Inventory Overview. Each then breakdown details and KPIs on their own page afterward.

###Production Overview
![Dashboard GIF](Demo/demo1.gif)
The dashboard is made according to the fiscal year terms, a custom date table was created using DAX, to automatically generate Fiscal year segregations. An assumption is made that the fiscal year starts on October 1st and ends on September 30th.  

This page gives information about the manufacturing overview of the company, Measures were created in Power BI in order to have custom KPIs. All the charts and KPIs are described below: -
Fiscal YTD - Waste:	The total number of products wasted during production for the whole fiscal year. This helps and gives an idea and a comparison to yearly waste goals.
Fiscal YTD - Production:	The total number of products manufactured during production for the whole fiscal year. This helps and gives an idea and a comparison to yearly production goals.
Average Production Lead Time:	The average latency between the initiation and completion of production. This helps determine where is the company investing the labor, which part of the assembly is taking more time in production, and if lead time can be reduced.
Fiscal YTD - Production Hours:	The total number of labor hours in production for the whole fiscal year. This helps and gives an idea and a comparison to yearly labor cost goals.
On-Time Production:	Percent of time when production goals were met. Helps and gives an idea of if the company is supplying the demand on time.
Waste Percent:	Percentage of products wasted during the manufacturing process.

### Charts on the page

- Cumulative Multiline chart showing Production totals helps compare the fiscal year production trends and helps remove bottlenecks in manufacturing.
- Donut Chart showing Actual cost distribution over different parts of the assembly line. Helps determine which parts cost more and where improvement is needed so that production costs are reduced.
- Waste cost by year line chart. A simple chart showing how money is the company wasting on discarded products and what is the trend.

### Category Analysis

After looking at the overview of the manufacturing department, one can navigate to the Product Category Page for a more detailed analysis. Which will help identify specific issues in the manufacturing system. 
This section consists of 4 charts that show an in-depth analysis of the Production components and help determine specific issues.
![Dashboard GIF](Demo/demo2.gif)

**Pareto Charts**
A Pareto chart is a Bar graph, the length of the chart represents frequency or cost, the longest bars are arranged on the left and the shortest to the right which amplifies the importance of the category with the highest bar. A line overlaps over the bar graph showing the percent contribution of the specific bar chart towards the total and the line accumulates the percent showing how many categories are important and consume most of the process. There are 2 Pareto Charts on this page, first is for the components required to manufacture a bike showing where most of the production is occupied and the other one is for the finished bike products showing categories of bikes produced.

**Waste Cost - Product Matrix Visual**
The Matrix visual shows the reason where exactly the waste is costing money to the company and due to which reasons. The first column provides the reason for waste, while the other two columns are divided into two categories Bikes (Actual bikes wasted in production) and Components (Components of bikes wasted in production). The Cost is conditionally formatted showing which portion is costing more and the reason for it. There are subtotals on rows and columns and grand total for total waste money.

**Bar chart**
A simple bar chart showing how many Product categories are produced on time.

### Inventory Overview
Another major component of the dashboard is the Inventory overview, although there is no data regarding the distribution supply chain in the database this analysis is done assuming the is one location.
![Dashboard GIF](Demo/demo3.gif)

The overview includes 3 KPI's, 3 Filters to slice the data, and 2 charts. 
**KPIs**
Fiscal YTD - Inventory Turnover:	The KPI tells us how many times did we make our product and then sold it. Technically how many productions and sales cycles did the inventory go through. 
Fiscal YTD - Inventory Value:	The cost of the inventory the company is holding at the current stage.
Fiscal YTD - Inventory Quantity:	The quantity of the inventory the company is holding at the current stage.

![Dashboard GIF](Demo/demo4.gif)
![Dashboard GIF](Demo/demo5.gif)
**Area Charts**
Area charts showing how much Inventory quantity and Inventory value does the company hold by the Assembly location category are shown in the area chart. This shows which part of the manufacturing is holding most of the money and if the company is making the right choices of investing in those parts. There is a button on top of the chart so the end-user can choose if he wants to view the quantity or value on the chart.

**Inventory Turnover Multiline chart**
Comparing inventory turnover on different fiscal years can show important data. It can help show the trends in previous years of how the inventory has been used and can help plan the production process in a better way.

## Conclusion
This dashboard delivers clear insights into manufacturing efficiency and inventory trends, enabling data-driven decisions that improve operations and reduce costs.


