# 🏪 Retail Analytics Power BI Dashboard

## 🧭 Project Overview
The **Retail Analytics Power BI Dashboard** delivers end-to-end insights into store performance, pricing, sales trends, and inventory management.  
It integrates multiple datasets to help executives, analysts, and operations teams make informed decisions on **sales growth**, **stock optimization**, and **profitability**.

This project highlights my ability to combine **data modeling, DAX, and Power BI visualization** to create a business intelligence solution that transforms raw data into actionable insights.

---

## 🎯 Objectives
- Build a centralized Power BI dashboard to monitor key business KPIs.  
- Identify trends in **sales, pricing, and demand forecasting**.  
- Improve **inventory control** through data-driven insights.  
- Analyze **regional and seasonal** performance drivers.  
- Empower decision-makers with interactive drillthrough and filtering options.

---

## 🧩 Dashboard Image Preview
Below are snapshots of the three main dashboard pages included in this project.

| Executive Overview | Inventory Management | Sales & Pricing Analytics |
|--------------------|----------------------|---------------------------|
| ![Executive Overview](https://raw.githubusercontent.com/donunobunjo/Retail_sales_and_inventory_dashboard/main/Images/Dashboard.PNG) | ![Inventory Management](https://raw.githubusercontent.com/donunobunjo/Retail_sales_and_inventory_dashboard/main/Images/inventory_mgt.png) | ![Sales & Pricing](https://raw.githubusercontent.com/donunobunjo/Retail_sales_and_inventory_dashboard/main/Images/sales_and_pricing.png) |

<p align="center">
  <em>Figure: Overview of the interactive Power BI dashboard pages.</em>
</p>

---

## ⚙️ Approach

### 🧮 Data Preparation & Modeling
- Cleaned and transformed raw data (Sales, Inventory, Product, Region) in **Power Query**.
- Built a **Star Schema**:
  - Fact Tables → `Sales`, `Inventory`
  - Dimension Tables → `Date`, `Store`, `Category`, `Region`
- Created relationships and applied filters for dynamic reporting.

### 📏 Key DAX Measures
Some key calculated metrics used across the dashboard:

```DAX
Total Sales = SUM(Sales[SalesAmount])

Average Selling Price = DIVIDE(SUM(Sales[SalesAmount]), SUM(Sales[UnitsSold]))

Profit Margin = DIVIDE(SUM(Sales[Profit]), SUM(Sales[SalesAmount]))

Inventory Turnover = DIVIDE(SUM(Sales[UnitsSold]), AVERAGE(Inventory[StockLevel]))

Sales Growth (YoY) = DIVIDE([Total Sales] - [Sales LY], [Sales LY])
