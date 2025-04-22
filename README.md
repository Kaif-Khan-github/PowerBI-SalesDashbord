# PowerBI-SalesDashbord
# 📊 Superstore Sales Analysis Dashboard (Power BI)

A comprehensive Power BI dashboard built to analyze and visualize sales data from a fictional superstore. This dashboard helps stakeholders identify trends, understand performance by region and product, evaluate the impact of discounts on profit, and segment customer behavior.

---

#Dataset Overview

- **Source**: [Superstore Sales Dataset](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final) (CSV format)
- **Records**: ~10,000 transactions
- **Fields**: Order ID, Order Date, Ship Mode, Customer Info, Region, State, Product Category/Sub-category, Sales, Profit, Discount, Quantity

---

#Objectives

- Visualize and explore sales and profit data interactively
- Identify top-performing regions, products, and customers
- Uncover loss-making areas (due to discounts or other factors)
- Provide actionable insights through visual storytelling

---

## 📂 Report Pages Breakdown

### 📍 **Page 1: KPI Overview**
**Visuals**: Card visuals

- **Total Sales**
- **Total Profit**
- **Average Discount**
- **Profit Margin** (custom DAX measure)
  
> Gives a quick, high-level view of business performance.

---

#**Page 2: Sales & Profit Trends**
**Visuals**: Line chart, Slicers

- **Line Chart** with Month on X-Axis, showing both `Sales` and `Profit`
- **Slicers**: Region and Category

> Helps identify trends over time and see how sales/profit vary by category or region.

---

#**Page 3: Regional Performance**
**Visuals**: Filled Map, Clustered Bar Chart

- **Map**: Profit visualized by State
- **Bar Chart**: Sales and Profit by Region

> Clearly identifies which regions/states are top performers and where profit is negative.

---

#*Page 4: Product Analysis**
**Visuals**: Treemap, Bar Chart, Slicer

- **Treemap**: Category/Sub-Category vs Sales
- **Bar Chart**: Top 10/Bottom 10 Products by Profit
- **Slicer**: Filter by Category

> Shows which product categories and sub-categories contribute the most to revenue and which products are underperforming.

---

#*Page 5: Discount vs Profit Analysis**
**Visuals**: Scatter Plot

- **X-Axis**: Discount
- **Y-Axis**: Profit
- **Size**: Sales
- **Color**: Product Category
- **Details**: Product Name (for individual dots)

> Analyzes how discounting affects profitability. Visualizes at what discount levels products start losing money.

---

#**Page 6: Customer Segment Insights**
**Visuals**: Stacked Column Chart, Table, Slicer

- **Stacked Column**: Segment-wise Sales and Profit
- **Table**: Customer Name, Sales, Profit, Discount
- **Slicer**: Region or Segment

> Helps understand customer behavior and profitability across different customer types like Consumer, Corporate, and Home Office.

---

# **Summary Page (Storyboard)**
**Visuals**: KPI Cards + Mini charts + Textboxes

- A final dashboard view bringing together key metrics and insights from all pages
- Includes takeaways such as:
  - "West region has the highest profit margin"
  - "High discounts (>30%) lead to consistent losses"
  - "Office Supplies drives sales, but Furniture yields more profit"

---

## 📊 Key DAX Measures Used

```dax
Profit Margin = DIVIDE(SUM(Sales[Profit]), SUM(Sales[Sales]))
