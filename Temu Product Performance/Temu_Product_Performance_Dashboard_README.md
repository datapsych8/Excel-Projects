# 🛍️ Temu Product Performance Dashboard

![Dashboard Preview](images/c:\Users\DataPsyched\Downloads\Temu Product performance dashboard - Made with Clipchamp.gif)

[![Excel](https://img.shields.io/badge/Built%20With-Microsoft%20Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)](https://www.microsoft.com/microsoft-365/excel)
[![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)]()
[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)]()
[![Made with 💡](https://img.shields.io/badge/Made%20with%20💡-Data%20Analysis%20and%20Visualization-orange?style=for-the-badge)]()

---

## 📘 Table of Contents
1. [Project Overview](#project-overview)
2. [Objectives](#objectives)
3. [Data Source](#data-source)
4. [Data Preparation & Cleaning](#data-preparation--cleaning)
5. [Data Modeling](#data-modeling)
6. [Dashboard Design](#dashboard-design)
7. [Key Insights](#key-insights)
8. [Challenges & Limitations](#challenges--limitations)
9. [Lessons Learned](#lessons-learned)
10. [Tools & Technologies](#tools--technologies)
11. [How to Use the Dashboard](#how-to-use-the-dashboard)
12. [Image Gallery](#image-gallery)
13. [Author](#author)
14. [License](#license)

---

## 🧠 Project Overview

The **Temu Product Performance Dashboard** is an interactive Excel-based business intelligence solution designed to analyze and visualize product performance across multiple categories on the **Temu platform**.  

It enables both **technical and non-technical stakeholders** to quickly understand:
- Which product categories perform best  
- The relationship between pricing, ratings, and sales  
- The share of top-performing products  
- How different subcategories contribute to overall performance  

📊 Built completely in **Excel** using:
- Pivot tables  
- DAX measures  
- Interactive slicers  
- KPIs and Treemap visualizations  

---

## 🎯 Objectives

1. Identify **top-performing product categories and subcategories**.  
2. Analyze the **relationship between price bands, ratings, and sales**.  
3. Provide insights into **top-performing vs low-performing products**.  
4. Create a clean, professional, and **interactive dashboard** for business storytelling.  

---

## 📊 Data Source

- Dataset: *Temu Product Dataset* (CSV/Excel format)  
- Fields include:
  - Product ID, Category, Subcategory  
  - Sales Volume  
  - Ratings  
  - Median Price  
  - Seller Flag (Top Seller, Normal, Low Sales)

![Data Preview](images/![alt text](image.png))

---

## 🧹 Data Preparation & Cleaning

Performed in **Excel Power Query**:

- Removed duplicates and irrelevant fields  
- Fixed inconsistent category names  
- Cleaned missing and outlier values  
- Standardized price and ratings columns  
- Created calculated columns for performance segmentation  

📘 Example of Calculated Columns:
```excel
=IF([@Sales_Volume]>AVERAGE(Sales_Volume),"Top Performer","Low Performer")
```

---

## 🧩 Data Modeling

- Data modeled using **Power Pivot**  
- Created relationships between:
  - Product Table  
  - Category Table  
  - Price Band Table  
- DAX Measures Created:
  - Total Sales Volume  
  - Total Products  
  - Median Price  
  - Average Ratings  
  - % of Top Performers  

📘 Example DAX Formula:
```DAX
Top_Performer% = 
DIVIDE(
    CALCULATE(COUNTROWS(Products), Products[Performance] = "Top Performer"),
    COUNTROWS(Products),
    0
)
```

---

## 🎨 Dashboard Design

The dashboard follows a **storytelling layout**, guiding the viewer through insights step by step.  

### 🔹 Layout Components:
| Section | Chart Type | Purpose |
|----------|-------------|----------|
| Top KPIs | Cards with Icons | Overview of key metrics |
| Chart 1 | Horizontal Bar Chart | Sales by Category |
| Chart 2 | Clustered Column Chart | Distribution of Performance |
| Chart 3 | Combo Chart | Relationship between Price & Sales |
| Chart 4 | Scatter Plot | Ratings vs Sales Volume |
| Chart 5 | Treemap | Subcategory Contribution |

### 🔹 Slicers Added:
- **Price Tier** (Ultra Low → Ultra High)  
- **Seller Flag** (Top Seller, Low Sales, Normal)  

---

## 💡 Key Insights

| Visualization | 2-Line Insight |
|----------------|----------------|
| **Sales by Category** | *Home & Kitchen dominates sales, contributing over a quarter of total volume. Jewelry & Accessories follows closely.* |
| **Performance by Category** | *Women's Clothing and Jewelry have the highest share of top performers.* |
| **Price vs Sales (Combo Chart)** | *Lower price bands (Ultra Low, Low) drive the highest total sales volume, showing affordability boosts performance.* |
| **Ratings vs Sales (Scatter)** | *Products with ratings above 4.0 tend to have disproportionately higher sales.* |
| **Treemap (Subcategories)** | *Office & School, Shoes, and Wellness categories make up the bulk of top-performing subcategories.* |

---

## ⚙️ Challenges & Limitations

| Challenge | Description |
|------------|--------------|
| Treemap Automation | Initially planned to automate Treemap with dynamic DAX but later opted for manual creation for simplicity. |
| Data Volume | Large dataset caused Excel lag during pivot updates. |
| Visual Clarity | Balancing detailed charts with clean layout took multiple iterations. |
| KPI DAX Integration | Some DAX formulas required recalibration due to column naming inconsistencies. |

---

## 🧭 Lessons Learned

1. The importance of **data cleaning and column standardization** before modeling.  
2. How to apply **DAX and pivot calculations** effectively in Excel.  
3. Dashboard storytelling must be **visually intuitive** for mixed audiences.  
4. Using filters like **Top 10%** improved clarity and focus.  
5. Sometimes **manual tweaks** (like the treemap) are better than over-automation.  

---

## 🧰 Tools & Technologies

| Tool | Purpose |
|------|----------|
| **Microsoft Excel (Power Pivot & Power Query)** | Data transformation & modeling |
| **DAX** | Advanced metric calculation |
| **Excel Charts & Slicers** | Visualization & interactivity |
| **Conditional Formatting** | KPI visualization |
| **GitHub Markdown + PDF Export** | Documentation |

---

## 🖱️ How to Use the Dashboard

1. Open the **Dashboard** sheet in Excel.  
2. Use slicers (Price Tier, Seller Flag) to filter visuals.  
3. Hover over charts for tooltip details.  
4. Click **Dataset Button** to view the underlying data table.  

📌 *All charts have a “Top 10% filter” applied to ensure focus on high-impact categories.*

---

## 🖼️ Image Gallery

- ![Dashboard Overview](images/dashboard_overview.png)
- ![KPI Section](images/kpi_cards.png)
- ![Pivot Table Example](images/pivot_example.png)
- ![Treemap Visualization](images/treemap.png)
- ![Data Model View](images/data_model.png)

---

## 👤 Author

**Andrew [GitHub: @yourusername]**  
📧 [your.email@example.com]  
💼 [LinkedIn Profile](#)  

---

## 📜 License

This project is licensed under the **MIT License** — feel free to fork, use, and build upon it with attribution.
