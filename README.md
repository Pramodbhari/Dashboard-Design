# Task 4 – Sales & Financial Dashboard (Power BI)

This repository contains my submission for **Task 4: Dashboard Design** for the Data Analyst Internship.

## 📌 Objective

Design an interactive **Sales & Financial dashboard** using Power BI to help business stakeholders understand:
- Overall Sales & Profit
- Profitability (Profit Margin %)
- Sales Growth over time
- Performance by Region, Segment, Category & Sub-Category

## 📂 Dataset

- **Source:** Kaggle – Superstore Sales Dataset  
- **Link:** https://www.kaggle.com/datasets/vivek468/superstore-dataset-final  
- **Key Columns:** Order Date, Ship Date, Category, Sub-Category, Segment, Region, Sales, Profit, Quantity, Discount

## 🧮 Power BI Measures (DAX)

Main measures used:

```DAX
Total Sales = SUM ( Orders[Sales] )

Total Profit = SUM ( Orders[Profit] )

Total Orders = DISTINCTCOUNT ( Orders[Order ID] )

Profit Margin % = DIVIDE ( [Total Profit], [Total Sales] )

Avg Discount % = AVERAGE ( Orders[Discount] )

Sales per Order = DIVIDE ( [Total Sales], [Total Orders] )

Sales LY = CALCULATE ( [Total Sales], SAMEPERIODLASTYEAR ( DateTable[Date] ) )

Sales YoY Growth = DIVIDE ( [Total Sales] - [Sales LY], [Sales LY] )

