# Ecommerce-Sales-Dashboard
# 📊 E-Commerce Sales Dashboard (Power BI)

### 🔹 A complete end-to-end data analysis project for my Data Analyst portfolio.

This project showcases my ability to clean data, create actionable business insights, and build an interactive Power BI dashboard.

---

## 🧾 **Project Overview**
I worked on an E-commerce sales dataset and built a Power BI dashboard that helps answer key business questions such as:

- Which product categories generate the highest revenue?
- What is the YTD sales & YTD profit trend?
- Which region contributes the most to sales?
- Top 5 and bottom 5 product by sales.
- YTD sales by region to know best and worst performing all over the country.
- YTD sales by shippin type to get the best and worst performing region all over the country.
- Create a KPI banner showing YTD sales , YTD profit , YTD quantity sold, YTD profit margin.
- Find YTD sales performance by each state 


The dashboard is fully interactive and provides clear insights for decision-making.

---

## 🧹 **Data Cleaning Steps (Power Query)**
In Power Query, I performed the following cleaning steps:

- Removed duplicates and null values  
- Standardized date formats  
- Extracted year, month, and week from date  
- Converted data types (numeric, text, date)  
- Created calculated columns:
  - Profit
  - Profit Margin
  - Sales Growth YoY
- Corrected category names and region information  

---

## 📊 **Dashboard Insights**
Some key insights discovered:

- 📈 **Sales show consistent upward and downward trend in YTD sales.**
- 🛍️ **The top-performing category is Office supplies in YTD sales .**
- 🌍 **The West region shows the highest sales.**
- 👥 **Standard class shipping type has more YTD sales .**
---

## 🔧 **Power BI Features Used**
- Power Query Editor  
- DAX Measures  
- Slicers & Filters  
- Conditional Formatting  
- Interactive charts & KPI cards  

---

## 🧮 **DAX Measures Created**
Some examples:

```DAX
YTD Sales = TOTALYTD(SUM(ecommerce_data[sales_per_order]),'Calendar'[Date])

YoY Sales = ([YTD Sales]-[PYTD Sales])/[PYTD Sales]

PYTD Sales = CALCULATE(SUM(ecommerce_data[sales_per_order]),DATESYTD(SAMEPERIODLASTYEAR('Calendar'[Date])))

YoY Profit = ([YTD Profit]-[PYTD Profit])/[PYTD Profit]

YTD Profit = TOTALYTD(SUM(ecommerce_data[profit_per_order]),'Calendar'[Date])
