# 🍕 Plato's Pizza Sales Analysis & Performance Dashboard

![Power BI](https://img.shields.io/badge/power_bi-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-00758F?style=for-the-badge&logo=powerbi&logoColor=white)
![Data Modeling](https://img.shields.io/badge/Data_Modeling-Subject?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)

## 📖 Project Overview
This project is part of the **Maven Pizza Challenge**. Acting as a BI Consultant for Plato's Pizza, a Greek-inspired pizzeria in New Jersey, I was tasked with analysing a year's worth of transactional data. The goal was to transform raw data into actionable insights to help the restaurant improve operational efficiency and increase sales.

## 🏹 Business Problem & Objectives
Plato's Pizza wants to transition to a data-driven decision-making process. The management specifically requested answers to the following key questions:
* **Peak Operations:** What days and times is the restaurant busiest?
* **Production:** How many pizzas are being made during peak periods?
* **Product Performance:** What are the best and worst-selling pizzas?
* **Financials:** What is the Average Order Value (AOV)?
* **Capacity Planning:** How well is the restaurant utilising its seating capacity (15 tables, 60 seats)?

## 📂 Data Structure & Modeling
The raw data consisted of transactional records including order dates, times, pizza types, sizes, quantities, prices, and ingredients.

### Data Transformations
1.  **Date Table:** Calculated a dedicated date table for Time Intelligence analysis (YTD, MoM).
2.  **Time Table:** Calculated a dedicated time table for granular hourly analysis.
3.  **Star Schema:** Developed a comprehensive data model connecting Fact tables (Order Details) with Dimension tables (Orders, Pizza, Pizza Type, dDate, dTime).

### Data Model Diagram
Below is the relationships view of the model created for this project:

<img width="1110" height="1010" alt="image" src="https://github.com/user-attachments/assets/944a275d-cb7f-4c4a-955d-5dc4820e7090" />

*Note: The model utilises a star/snowflake schema approach to optimise query performance and filter propagation.*

## 📐 Key Measures & DAX Calculations
Extensive DAX measures were written to analyse performance across three main pillars:

### 1. Item Analysis
* **Volume:** `Items_Sold`, `Items_Sold_YTD`, `Average_Items_Per_Day`.
* **Peaks:** `Busiest Day & Time` (logic based on item volume).
* **Ranking:** `Best Selling Items` and `Least Selling Items` (by volume).
* **Growth:** `% MoM Items Sold`.

### 2. Revenue Analysis
* **Sales:** `Total Revenue`, `Revenue YTD`.
* **Ranking:** `Best/Least Selling Product` (by revenue).
* **Growth:** `% MoM Revenue`.

### 3. Order Analysis
* **Metrics:** `Number of Orders`, `Orders YTD`, `Average Order Value (AOV)`.
* **Growth:** `% MoM Orders`.

*Technical Feature: Measure Parameters were utilised to allow users to switch between metric views on visuals dynamically.*

## 📊 Dashboard Visuals & Navigation
The report features a side navigation panel that allows users to switch between **Items**, **Revenue**, and **Order Details**.

### 🔹 Page 1: Items Analysis
Focused on operational volume and product popularity.
<img width="2569" height="1454" alt="image" src="https://github.com/user-attachments/assets/bc824754-2e4c-40a2-9e70-53fc281f09ae" />

* **KPI Cards:** Total Revenue, AOV, Total Orders, Total Items Sold, and Peak Metrics (Busiest Day/Hour & Item count during that peak).
* **Categorical Analysis:** Bar charts for Items Sold by Category and Pizza Size.
* **Trend Analysis:** Line chart for Monthly Items Sold vs. Revenue.
* **Operational Heatmap:** A matrix showing Day vs. Hour intensity. Includes buttons to toggle the heatmap values between Orders, Items Sold, and Average Items.
* **Top/Bottom Performers:** Cards highlighting Best and Worst selling items by both Units and Revenue.

### 🔹 Page 2: Revenue Analysis
Focused on financial performance.
<img width="2575" height="1460" alt="image" src="https://github.com/user-attachments/assets/306b3dc8-f16e-4c1d-9f6a-3774b4417fa5" />

* **Breakdowns:** Revenue by Category and Pizza Size.
* **Top Performers:** Top 5 Pizzas by Revenue.
* **Comprehensive Matrix:** A detailed monthly view showing Orders, %MoM Orders, Items Sold, %MoM Items, Revenue, and %MoM Revenue alongside YTD figures.

### 🔹 Page 3: Order Details
Focused on granular data for auditing and deep dives.
<img width="2575" height="1458" alt="image" src="https://github.com/user-attachments/assets/626500d8-2dff-4e2b-9977-2b78c4dd1bf7" />

* **Temporal Analysis:** Bar charts for Orders by Day and Orders by Hour.
* **Detail Matrix:** A tabular view listing Order Date, Hour, Order ID, Category, Size, Quantity, and Revenue.

## 🛠 Tools Used
* **Power BI Desktop:** For data modelling, visualisation, and interactivity.
* **Power Query:** For ETL (Extract, Transform, Load) processes.
* **DAX (Data Analysis Expressions):** For complex calculations and time intelligence.

## ℹ️ Model Dictionary
A complete model dictionary was generated for this project, detailing all measures, tables, columns, and relationships to ensure maintainability and clarity for future developers.

## 🤝 Acknowledgments
This project was created as part of the **Maven Pizza Challenge**.
* **Challenge Page:** [Maven Analytics Pizza Challenge](https://mavenanalytics.io/challenges/maven-pizza-challenge)
* **Dataset:** Provided by Maven Analytics to simulate a real-world business scenario.

---
*Created by Felix Ocham| [Linkedin Profile](https://www.linkedin.com/in/felix-o-703987a7/)*
