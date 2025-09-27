# 📊 Superstore Sales Analysis Dashboard

## Overview

This repository contains the data and documentation for a comprehensive **Superstore Sales Analysis Dashboard** built with **Power BI**. The dashboard provides a detailed overview of the sales performance of a fictional superstore, offering insights into sales trends, profitability, customer behavior, and regional performance.

The primary goal of this project is to consolidate and visualize sales data to empower business leaders to make data-driven decisions, identify areas for improvement, and discover growth opportunities.

---

## 📁 Data Sources

The dashboard is built using three core datasets, which provide a holistic view of the superstore's operations:

1.  **`Orders.csv`**: The main transactional dataset. This file contains detailed information for every order placed.
    * **Key Columns**: `Order ID`, `Order Date`, `Customer ID`, `Segment`, `Region`, `Product ID`, `Sales`, `Quantity`, `Discount`, `Profit`.

2.  **`Returns.csv`**: This dataset contains information about which orders were returned.
    * **Key Columns**: `Order ID`, `Returned`.

3.  **`People.csv`**: This dataset includes information about the regional sales managers.
    * **Key Columns**: `Person`, `Region`.

---

## 📈 Power BI Dashboard & Visualizations

The Power BI dashboard is designed to be intuitive and interactive, allowing users to drill down into the data and explore various facets of the business. The main dashboard page provides a high-level summary, with options to navigate to more detailed reports.

### Key Visualizations Include:

* **KPI Cards**: At-a-glance view of critical metrics such as *Total Sales*, *Total Profit*, *Profit Margin*, and *Total Orders*.
* **Sales & Profit Over Time**: A line chart that visualizes monthly or quarterly sales and profit trends, helping to identify seasonality and growth patterns.
* **Sales by Region Map**: A geographical map that displays sales and profit distribution across different regions.
* **Top Products & Customers**: Bar charts or tree maps showcasing the most profitable products and the customers contributing the most to revenue.
* **Sales by Category/Sub-Category**: A donut or bar chart that breaks down sales by product category.
* **Profitability Analysis**: A scatter plot analyzing the relationship between sales, discounts, and profit to identify sources of profit leakage.

---

## ⚙️ Data Model

The data model in Power BI is structured to enable robust analysis. The tables are linked through the following relationships:

* The **`Orders`** table is the central fact table.
* The **`Returns`** table is linked to the **`Orders`** table using a one-to-one relationship based on the `Order ID` column.
* The **`People`** table is linked to the **`Orders`** table using a many-to-one relationship based on the `Region` column, allowing for analysis of sales performance by regional manager.
