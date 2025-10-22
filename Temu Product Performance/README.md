# 🛍️ Temu Product Performance Dashboard

![Dashboard Overview](https://github.com/user-attachments/assets/5b88e101-517d-4cc4-bd1b-b9408177f8fa)
 

[![Excel](https://img.shields.io/badge/Built%20With-Microsoft%20Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)](https://www.microsoft.com/microsoft-365/excel)
[![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)]()
[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](./LICENSE)
[![Made with 📊](https://img.shields.io/badge/Made%20with%20📊-Data%20Storytelling%20%26%20Visualization-orange?style=for-the-badge)]()

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

<img width="967" height="487" alt="Dataset snapshot" src="https://github.com/user-attachments/assets/487244b2-c2de-415b-9f9f-ecdb7d6b3694" />


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
<img width="1578" height="327" alt="Performaers Formula" src="https://github.com/user-attachments/assets/bb04f678-c872-48d4-b223-c649ff2644e3" />

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
<img width="644" height="438" alt="Dax formula" src="https://github.com/user-attachments/assets/90cde374-575f-4314-9b3d-86b7f46451ec" />

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

<img width="1559" height="699" alt="Dashboard" src="https://github.com/user-attachments/assets/9cdb9c81-885f-4f37-9454-adf400d9f11b" />

### 🔹 Slicers Added:
- **Price Tier** (Ultra Low → Ultra High)  
- **Seller Flag** (Top Seller, Low Sales, Normal)
  
<img width="298" height="243" alt="Slicers" src="https://github.com/user-attachments/assets/02e9014f-3244-4133-a3bb-dd178789de6b" />

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
| **GitHub Markdown + Powerpoint for Presentation** | Documentation |

---

## 🖱️ How to Use the Dashboard

1. Open the **Dashboard** sheet in Excel.  
2. Use slicers (Price Tier, Seller Flag) to filter visuals.  
3. Hover over charts for tooltip details.  
4. Click **Dataset Button** to view the underlying data table.  

📌 *All charts have a “Top 10% filter” applied to ensure focus on high-impact categories.*

---

## 🖼️ Image Gallery

- ![Dashboard Overview](https://github.com/user-attachments/assets/5b88e101-517d-4cc4-bd1b-b9408177f8fa)
- <img width="976" height="78" alt="Kpi card" src="https://github.com/user-attachments/assets/47f4b37e-75fd-43fd-8d75-d3769858d309" />
- <img width="1058" height="313" alt="pivot table snapshot" src="https://github.com/user-attachments/assets/4b128488-ef6e-43df-ba2d-4d18abfd756e" />
- <img width="313" height="285" alt="Treemap" src="https://github.com/user-attachments/assets/506e1ede-f068-4fa2-acfc-77daa74e9e96" />
- <img width="1505" height="684" alt="Data Model" src="https://github.com/user-attachments/assets/07febf61-3bd8-4a04-8e3a-b7b1b8eeda8b" />

---

## 👤 Author

**Andrew [GitHub: @datapsych8)]**  
📧 [Email Address](dataspych234@gmail.com)  
💼 [LinkedIn Profile](www.linkedin.com/in/datapsych)  

---

## 📜 License

This project is licensed under the **MIT License** — feel free to work, use, and build upon it with attribution.
