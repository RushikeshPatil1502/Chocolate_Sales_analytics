# 🍫 Power BI Portfolio Project – Chocolate Sales Analysis

This project showcases an **interactive Power BI dashboard** designed to analyze **chocolate sales performance** using advanced **DAX measures** and **visual storytelling techniques**.  
It highlights trends in **shipments, profit percentage, and product performance**, providing deep business insights.

---

## 📊 Dashboard Preview

![Chocolate Sales Analysis Dashboard](Assets/Chocolate_sale_analysis.png)

---

## 🚀 Features

- 📦 **Low Box Shipments Analysis**  
  Identify and monitor shipment efficiency across regions and time periods.

- 💰 **Profit Percentage Metrics**  
  DAX-driven calculations for margin, revenue, and cost performance.

- 📈 **Dynamic Tables and Visuals**  
  Drill-down reports, bar charts, KPIs, and category-wise insights.

- 🎚️ **Interactive Slicers and Selectors**  
  Filter data dynamically by region, date, category, or shipment type.

- 🧮 **Custom DAX Measures**  
  Includes formulas for:
  - Profit %
  - Shipment Counts
  - Revenue per Category
  - Variance & Growth Rate

---

## 🧠 DAX Highlights

Some of the key DAX expressions used:
```DAX
Profit % = DIVIDE(SUM(Sales[Profit]), SUM(Sales[Revenue]), 0)
Low Box Shipments = CALCULATE(COUNT(Sales[Shipment_ID]), Sales[Boxes] < 5)
Revenue Growth % = DIVIDE(SUM(Sales[Revenue]) - CALCULATE(SUM(Sales[Revenue]), DATEADD(Sales[Date], -1, YEAR)), CALCULATE(SUM(Sales[Revenue]), DATEADD(Sales[Date], -1, YEAR)))
