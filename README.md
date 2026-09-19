# 🛒 E-Commerce Sales Dashboard – Power BI

## 📊 Project Overview

This project is an interactive **E-Commerce Sales Dashboard** created using **Microsoft Power BI**.

The dashboard analyzes e-commerce sales performance across products, categories, regions, payment methods, customer types, cities, and months.

The project demonstrates practical skills in **data preparation, data modeling, DAX, data visualization, KPI analysis, and interactive dashboard development**.

## 🛠️ Tools & Technologies

- Microsoft Power BI
- Power Query
- DAX
- Data Modeling
- Star Schema
- Data Visualization
- Interactive Slicers

## 🗂️ Data Model

The project uses a **Star Schema** consisting of one fact table and three dimension tables.

### Fact Table

**FactOrders**

- Order ID
- Order Date
- Product ID
- Customer ID
- Region
- Payment Method
- Quantity
- Sales

### Dimension Tables

**DimProduct**

- Product ID
- Product
- Category
- Price

**DimCustomer**

- Customer ID
- Customer Name
- City
- Customer Type

**DimDate**

- Date
- Year
- Month Number
- Month Name
- Quarter

## 🔗 Relationships

The following relationships were created:

- DimProduct → FactOrders
- DimCustomer → FactOrders
- DimDate → FactOrders

All relationships use **One-to-Many (1:*)** cardinality with **Single** filter direction.

## 🧮 DAX Measures

### Total Sales

```DAX
Total Sales = SUM(FactOrders[Sales])

## Total Quantity
Total Quantity = SUM(FactOrders[Quantity])

## Average Order Value
Average Order Value = AVERAGE(FactOrders[Sales])

## Total Orders
Total Orders = DISTINCTCOUNT(FactOrders[Order ID])

##Author
Reshma

