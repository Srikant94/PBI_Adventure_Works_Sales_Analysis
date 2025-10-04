# 🚴‍♂️ AdventureWorks Sales & Customer Performance Dashboard

### 📊 Built with Power BI | Data Cleaning in Power Query | Modeling in Power Pivot | DAX for KPIs  

## 📁 Project Overview

The **AdventureWorks Power BI Dashboard** is a comprehensive business intelligence solution designed to analyze and visualize the sales performance, customer behavior, and product profitability for **AdventureWorks**, a global bicycle and accessories retailer.  

This project was built as part of my **Power BI Desktop course by Maven Analytics**, focusing on transforming raw data into actionable business insights through **data modeling, DAX measures, and interactive dashboards**.

## 🎯 Business Problem

AdventureWorks faced challenges understanding:
- Which product categories drive the most **revenue and profit**
- Who are their **top-performing customers**
- Which products have **high return rates**
- How **sales trends** evolved from 2020–2022  

The goal was to develop an **executive-friendly dashboard** that could be used to:
- Track KPIs at a glance  
- Identify sales and profit trends  
- Understand customer segments  
- Optimize product and marketing strategies  

## 🧩 Data Sources

- `Sales.csv`
- `Products.csv`
- `Customers.csv`
- `Returns.csv`

All files were cleaned and transformed using **Power Query**, and modeled in **Power Pivot** using a **star schema** design.

## 🧮 Data Modeling

**Model Type:** Star Schema  
**Fact Table:** Sales  
**Dimension Tables:** Customers, Products, Returns, Date  

**Relationships:**
- `Sales[CustomerKey]` → `Customers[CustomerKey]`
- `Sales[ProductKey]` → `Products[ProductKey]`
- `Sales[OrderDate]` → `Date[Date]`
- `Returns[ProductKey]` → `Products[ProductKey]`

## 🧠 DAX Measures

Here are a few core **DAX measures** created in Power BI:

```DAX
-- Total Revenue
Total Revenue = SUM(Sales[SalesAmount])

-- Total Profit
Total Profit = SUM(Sales[Profit])

-- Total Orders
Total Orders = COUNTROWS(Sales)

-- Return %
Return % = DIVIDE(COUNTROWS(Returns), COUNTROWS(Sales), 0)

-- Revenue per Customer
Revenue per Customer = DIVIDE([Total Revenue], DISTINCTCOUNT(Sales[CustomerKey]), 0)

🖥️ Dashboards Overview
1️⃣ Executive Dashboard

Highlights:

KPIs: Total Revenue ($24.9M), Profit ($10.5M), Orders (25.2K), Return % (2.17%)

Year-over-year sales and profit trends

Category-wise order breakdown

Top 10 products by revenue and profit

2️⃣ Customer Dashboard

Highlights:

17.4K unique customers analyzed

Segmentation by income and occupation

Top customers driving revenue and profit

Interactive slicers for trend analysis

3️⃣ Product Dashboard

Highlights:

Product performance across time

Profitability and cost analysis

“Price Adjustment %” simulation

Return % per product line

💡 Key Insights

✅ Revenue and profit showed steady growth from 2020–2022
✅ Bikes category drives the most revenue; accessories lead in order volume
✅ “Shorts” show high return rates — indicating potential quality issues
✅ Top customers contribute significantly to overall revenue
✅ Marketing efforts should focus on high-value repeat buyers

📈 Business Recommendations

Focus marketing on high-value customers

Investigate return causes in the clothing category

Expand bike & accessory lines — the most profitable categories

Consider loyalty programs for repeat customers

🏁 Outcomes

Built 3 professional, interactive dashboards

Strengthened skills in data modeling, DAX, and storytelling

Delivered a clear, actionable business intelligence solution
