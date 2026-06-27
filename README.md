# MaykInvest-Power-BI_Hardware_Store

# 🏪 MaykInvest - Power BI Hardware Store Analytics

## 📊 Project Overview

**MaykInvest-Power-BI_Hardware_Store** is a data analytics project designed to simulate a real-world hardware store business environment. The goal is to transform raw transactional data into actionable insights using Power BI, following industry-standard data modeling and visualization practices.

This project focuses on building a **scalable and maintainable reporting solution**, applying concepts such as:

* Star schema data modeling (fact and dimension tables)
* Data transformation using Power Query (ETL process)
* Parameterized data source configuration (BasePath)
* Interactive dashboards for business decision-making

---

## 🎯 Objectives

* Analyze sales performance across products, customers, and time
* Identify revenue trends and seasonality patterns
* Evaluate supplier and inventory performance
* Monitor returns and support impact on business metrics
* Provide clear and interactive dashboards for stakeholders

---

## 🧱 Data Architecture

The project is structured using a **star schema**, ensuring performance and clarity:

* **Fact Tables**

  * `fact_sales`
  * `fact_returns`
  * `fact_support`

* **Dimension Tables**

  * `dim_customers`
  * `dim_products`
  * `dim_suppliers`
  * `dim_inventory`
  * `dim_promotions`

This approach improves query performance and aligns with best practices in BI systems.


# 🚀 Power BI Project Setup Guide

This project uses a **parameterized data source approach** to ensure portability across different environments (e.g., different machines, team members, or deployment setups).

Instead of hardcoding file paths, we use a **BasePath parameter**, allowing each user to configure their local data directory without modifying queries.

---

## 📂 Project Structure

Ensure the following structure is maintained after downloading or cloning the repository:

```
Project/
 ┣ data/"tables here in this folder"
 ┗ report.pbix
```
---

## ⚙️ How to Configure on a New Machine

Follow these steps to correctly connect the report to your local data:

Step 1 → Download or clone the project folder
Step 2 → Keep the folder structure unchanged

Step 3 → Open `report.pbix` in Power BI Desktop

Step 4 → Click **Transform Data / Home tab**
Step 5 → Click **Manage Parameters**

Step 6 → Update the `BasePath` parameter to your local data folder

Example:

```
C:\Users\MyPC\Desktop\Projects\MaykInvest-Power-BI_Hardware_Store\data
```

Step 7 → Click **OK**

Step 8 → Click **Refresh**

Step 9 → Done ✅

---

## 🧠 Why This Approach?

* Eliminates hardcoded paths
* Makes the project portable
* Simplifies collaboration
* Reduces setup time for new environments

---

## ⚠️ Notes

* Do not rename the `data` folder unless you update the parameter accordingly
* Ensure all required CSV files are present before refreshing
* If refresh fails, verify the `BasePath` value

---

## 💡 Best Practice

Always use parameters for external dependencies (paths, APIs, credentials).
This keeps your data models **scalable, maintainable, and production-ready**.



