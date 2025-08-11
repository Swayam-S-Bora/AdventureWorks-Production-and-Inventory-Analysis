# AdventureWorks-Production-and-Inventory-Analysis

## Overview

This analysis goes through the Production and Inventory Analysis of the Microsoft AdventureWorks Database. Adventure Works is a fictional bicycle manufacturing company. This database contains standard transaction data from an Enterprise Resource Planning (ERP) system. It contains data from the following scenarios of the company: Human Resources, Product Management, Manufacturing, Purchasing, Inventory, Sales, and Admin.

This analysis focuses on the Manufacturing and Inventory part of the data. Microsoft Power BI has been used to create an interactive dashboard while pulling data from SQL Server.

## Data Source

[Data Source](https://docs.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver15&tabs=ssms)

## Data Model

<img width="620" alt="DataModel" src="/Demo/Data Model.png">

## Built With

- [Power BI](https://powerbi.microsoft.com/en-us/)  
- [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)

## Detailed Analysis

### Tables Used in the Model

- **Production Location** – Production assembly data (parts used to manufacture each product, with assembly location category)
- **Production Product** – Product details (physical specifications, price, etc.)
- **Production ProductCategory** – Product categories
- **Production ProductSubcategory** – Product subcategories
- **Production ProductInventory** – Inventory data of produced products
- **Production ScrapReason** – Waste data related to manufacturing
- **Production WorkOrder** – Production transactions and related data
- **Production WorkOrderRouting** – Production work order scheduling data and details
- **Sales SalesOrderDetail** – Transactional sales data

## Analysis

This dashboard analyzes manufacturing and inventory operations. It is designed with an app-like navigational interface. The main page links to two areas: **Production Overview** and **Inventory Overview**, each with its own KPIs and detailed breakdown.

---

### Production Overview

![Dashboard GIF](Demo/demo1.gif)

The dashboard uses fiscal year terms. A custom date table was created using DAX to automatically generate fiscal year segments, assuming the fiscal year starts on **October 1st** and ends on **September 30th**.

**KPIs on this Page:**

- **Fiscal YTD – Waste:** Total products wasted during production for the fiscal year.  
- **Fiscal YTD – Production:** Total products manufactured during the fiscal year.  
- **Average Production Lead Time:** Average time between production initiation and completion.  
- **Fiscal YTD – Production Hours:** Total labor hours in production for the fiscal year.  
- **On-Time Production:** Percentage of time when production goals were met.  
- **Waste Percent:** Percentage of products wasted during manufacturing.

**Charts:**

- **Cumulative Multiline Chart** – Compares fiscal year production trends to identify bottlenecks.  
- **Donut Chart** – Shows actual cost distribution across assembly line parts.  
- **Waste Cost by Year (Line Chart)** – Tracks monetary waste trends over time.

---

### Category Analysis

![Dashboard GIF](Demo/demo2.gif)

**Pareto Charts:**  
Two Pareto charts — one for bike manufacturing components, another for finished bike products — showing which categories contribute most to production volume.

**Waste Cost – Product Matrix Visual:**  
Matrix showing waste reasons, split into Bikes and Components, with conditional formatting to highlight cost impact.

**Bar Chart:**  
Shows the count of product categories produced on time.

---

### Inventory Overview

![Dashboard GIF](Demo/demo3.gif)

The inventory overview assumes a single location due to the absence of supply chain data in the database.

**KPIs:**

- **Fiscal YTD – Inventory Turnover:** Number of production-sales cycles completed.  
- **Fiscal YTD – Inventory Value:** Total cost of inventory on hand.  
- **Fiscal YTD – Inventory Quantity:** Total quantity of inventory on hand.

![Dashboard GIF](Demo/demo4.gif)  
![Dashboard GIF](Demo/demo5.gif)

**Area Charts:**  
Displays inventory quantity and value by assembly location category. Users can toggle between viewing quantity or value.

**Inventory Turnover Multiline Chart:**  
Compares turnover across fiscal years to reveal trends and aid production planning.

---

## Conclusion

This dashboard delivers clear insights into manufacturing efficiency and inventory trends, enabling data-driven decisions that improve operations and reduce costs.
