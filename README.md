# 🚗 BMW Sales Dashboard | Power BI Project


You can view the Power BI report using the following link:

[Power BI Report](https://app.powerbi.com/links/bVSKXwdq0H?ctid=f27f8f85-2e4d-48c9-a159-477768221df8&pbi_source=linkShare&bookmarkGuid=062dafa1-d0fa-43a3-8d53-ffc95726758a)

Feel free to explore the data and visualizations.



![Image](https://github.com/user-attachments/assets/c582eb18-75ef-40a2-a12f-98b58231a4e1)






Welcome to the BMW Sales Dashboard — a powerful and interactive business intelligence tool built using Power BI. This project focuses on analyzing BMW sales data using advanced DAX measures and compelling visual storytelling to empower stakeholders with actionable insights.

---

## 📚 Content

- [📊 Dashboard Overview](#-dashboard-overview)
- [🔍 Key Features](#-key-features)
- [📈 Business Insights Delivered](#-business-insights-delivered)
- [🧮 Key DAX Measures Used](#-key-dax-measures-used)
- [🗂️ Data Model & Schema](#️-data-model--schema)
- [📌 Tools & Technologies](#-tools--technologies)
- [📷 Screenshots](#-screenshots)
- [📁 Project Structure](#-project-structure)
- [🧑‍💻 Author](#-author)

---

## 📊 Dashboard Overview

This dashboard is designed to uncover key sales performance metrics across different time periods. It offers intuitive navigation and a clean user interface that makes it easy to explore trends, compare periods, and draw business conclusions.

---

## 🔍 Key Features

- ✅ **Interactive Filters** for Year, Month, and Day  
- 📅 **Dynamic Calendar Table** to leverage Power BI’s time intelligence capabilities  
- 📈 **Visual Analysis** of Revenue, Quantity Sold, and Average Price  
- 🔁 **Bookmarks & Action Buttons** for seamless page-to-page navigation  
- ⬆️⬇️ **Growth Indicators** with intuitive arrow visuals  
- 🎯 Designed for both **high-level executive insights** and **detailed sales analysis**

---

## 📈 Business Insights Delivered

- Identify **monthly and seasonal trends** in sales performance  
- Detect **underperforming months** using variance indicators  
- Track **revenue growth**, **average prices**, and **quantity sold** at a glance  
- Support **data-driven decisions** through intuitive visual design

---

## 🧮 Key DAX Measures Used

- `Revenue`  
- `Revenue Growth %`  
- `Revenue Variance %`  
- `Quantity Sold`  
- `Average Price`  
- `Variance Arrow Indicator`  
- `Previous Month Revenue`, `Same Period Last Year`  
- Time intelligence functions: `CALCULATE`, `DATEADD`, `TOTALYTD`, `PREVIOUSMONTH`, etc.

---

## 🗂️ Data Model & Schema

The data model follows a **Star Schema**, centered around a single fact table (`Fact_Tabl`) connected to multiple dimension tables. This structure enables efficient filtering, aggregation, and time intelligence.

### 🔸 Fact Table: `Fact_Tabl`

| Column Name     | Description                    |
|-----------------|--------------------------------|
| ChannelID       | Foreign key for sales channel  |
| CountryID       | Foreign key for country        |
| Date            | Transaction date               |
| ModelID         | Foreign key for BMW model      |
| Quantity Sold   | Number of units sold           |
| Total           | Total revenue from sales       |
| Unit Price      | Price per unit                 |

---

### 🔹 Dimension Table: `dimCountry`

| Column Name | Description                    |
|-------------|--------------------------------|
| Country     | Name of the country            |
| CountryID   | Primary key                    |
| Flag        | Flag image/icon                |
| Region      | Region (e.g., Europe, Asia)    |

---

### 🔹 Dimension Table: `dimChannel`

| Column Name | Description                |
|-------------|----------------------------|
| Channel     | Sales channel type         |
| ChannelID   | Primary key                |

---

### 🔹 Dimension Table: `dimModel`

| Column Name | Description                  |
|-------------|------------------------------|
| img         | Model image                  |
| Model       | BMW car model name           |
| ModelID     | Primary key                  |

---

### 🔹 Date Dimension Table: `Calendar`

| Column Name | Description                      |
|-------------|----------------------------------|
| Date        | Calendar date                    |
| Month       | Month name (e.g., Jan, Feb)      |
| Monthnum    | Month number (1–12)              |
| Qtr         | Quarter (Q1, Q2, Q3, Q4)         |
| Weekday     | Day of the week                  |

---

### 🔗 Relationships

- `Fact_Tabl[ChannelID]` → `dimChannel[ChannelID]`  
- `Fact_Tabl[CountryID]` → `dimCountry[CountryID]`  
- `Fact_Tabl[ModelID]` → `dimModel[ModelID]`  
- `Fact_Tabl[Date]` → `Calendar[Date]`

All relationships are **one-to-many** from dimension to fact table.

---

## 📌 Tools & Technologies

- **Power BI Desktop**
- **DAX (Data Analysis Expressions)**
- **Data Modeling**
- **Bookmarks & Navigation**
- **Calendar Table for Time Intelligence**

---

## Dashboard Overview
![Image](https://github.com/user-attachments/assets/43b955a3-27b2-4419-9343-d2c194357b5b)
![Image](https://github.com/user-attachments/assets/d866e696-f8d9-422f-a826-ad60c0a5587b)
![Image](https://github.com/user-attachments/assets/b2ce6577-20f1-45ff-92fe-38eb27418777)
---

## 📁 Project Structure

```bash
BMW-Sales-Dashboard/
│
├── BMW_Sales_Dashboard.pbix        # Power BI Dashboard file
├── README.md                       # Project documentation
├── images/                         # Screenshots for visual preview
│   ├── dashboard-overview.png
│   └── revenue-trends.png
└── data/
    └── BMW_Sales_Data.csv          # Source sales dataset (if public)
```

## 📥 How to Use / Clone This Repo


```bash
# Open your terminal / command prompt
git clone https://github.com/Akshay8087/BMW-Sales-Dashboard.git
```

