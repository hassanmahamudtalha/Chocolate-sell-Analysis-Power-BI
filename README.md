# Chocolate Sales Data - Power BI Report

## 📌 Project Overview

This Power BI report provides an in-depth analysis of chocolate sales data, including trends, key performance indicators (KPIs), and month-over-month (MoM) changes. The report is designed to help stakeholders make data-driven decisions by visualizing sales performance and identifying patterns.

## 📂 Dataset

- **Source:** Chocolate sales data
- **Format:** Imported into Power BI (.pbix)
- **Key Columns:**
  - Date
  - Product Name
  - Sales Quantity
  - Sales Revenue
  - Region
  - Customer Segment

## 📊 Key Measures (DAX)

### 1️⃣ Total Boxes Sold

```DAX
Total Boxes = SUM(Sales[Quantity])
```

### 2️⃣ Month-Over-Month (MoM) Change in Total Boxes (%)

```DAX
MOM chg(Total Boxes)% =
VAR This_month = [Total Boxes]
VAR Pre_month = CALCULATE([Total Boxes], PREVIOUSMONTH('Calendar'[Date]))
RETURN DIVIDE(This_month - Pre_month, Pre_month)
```

### 3️⃣ Total Revenue

```DAX
Total Revenue = SUM(Sales[Revenue])
```

### 4️⃣ Average Revenue Per Sale

```DAX
Avg Revenue Per Sale = DIVIDE([Total Revenue], [Total Boxes])
```

## 📈 Visualizations

- **KPI Cards:**
  - Total Boxes Sold
  - MoM Change (%)
  - Total Revenue
  - Avg Revenue Per Sale
- **Line Charts:**
  - Sales Trends Over Time
- **Bar Charts:**
  - Sales by Region
  - Top-Selling Products
- **Tables:**
  - Sales Breakdown by Month
- **Filters & Slicers:**
  - Date Range
  - Product Name
  - Region
  - Customer Segment

## 🛠️ How to Use

1. Download and open the `.pbix` file in Power BI Desktop.
2. Ensure your dataset is properly connected.
3. Navigate through the different visualizations to explore sales trends.
4. Use filters and slicers to customize your analysis.

## 🔍 Troubleshooting

- **Issue:** MoM Change (%) not displaying correctly.
  - **Solution:** Ensure the calendar table is correctly linked to the sales data.
  - Check if `Calendar[Date]` has continuous date values.
![Screenshot 2025-03-09 203428](https://github.com/user-attachments/assets/d41ca755-dd84-44a5-863b-ac141955dbdc)


https://github.com/user-attachments/assets/8dc5c32c-b357-402e-b960-81c45b01706c







