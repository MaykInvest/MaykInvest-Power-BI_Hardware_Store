# 🏪 MaykInvest - Power BI Hardware Store Analytics

## 📊 Project Overview

**MaykInvest-Power-BI_Hardware_Store** is a data analytics project designed to simulate a real-world hardware store business environment. The goal is to transform raw transactional data into actionable insights using Power BI, following industry-standard data modeling and visualization practices.

This project focuses on building a **scalable and maintainable reporting solution**, applying concepts such as:

* Star schema data modeling (fact and dimension tables)
* Data transformation using Power Query (ETL process)
* Parameterized data source configuration (`URL_FILES`)
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

The project is structured using a **star schema**, ensuring performance and clarity.

### Fact Tables

* `fact_inventory`
* `fact_purchases`
* `fact_returns`
* `fact_sales`
* `fact_support`

### Dimension Tables

* `dim_customers`
* `dim_products`
* `dim_promotions`
* `dim_suppliers`

This approach optimizes query performance and aligns with industry best practices in BI systems.

---

## 🚀 Power BI Project Setup Guide

This project uses a **parameterized data source approach** to ensure portability across different environments (e.g., different machines, team members, or deployment setups).

Instead of hardcoding individual file paths, a central parameter called **`URL_FILES`** is used. This allows each user to configure their local data directory directly through the Power BI interface without modifying query code.

---

## 📂 Project Structure

Ensure the following folder structure is maintained after downloading or cloning the repository:

```text
Project/
 ┣ data/ # All CSV data files must be stored here
 ┗ report.pbix
```

---

## ⚙️ Configuration Guide (New Machine Setup)

Follow the steps below to connect the report to your local environment.

### 🔹 Part 1: Setting Up the Parameter

1. Open `report.pbix` in Power BI Desktop
2. Navigate to the **Home** tab
3. Click **Manage Parameters → New Parameter**
4. Configure the parameter:

   * **Name:** `URL_FILES`
   * **Description:** Central path for project data files
   * **Type:** Text
   * **Current Value:** Your local data folder path

   **Example:**

   ```
   C:\Users\MyPC\Desktop\Projects\MaykInvest-Power-BI_Hardware_Store\data\
   ```

---

### 🔹 Part 2: Linking Tables Dynamically

5. Select a table (e.g., `dim_customers`) from the Queries panel

6. Go to **Home → Data Source Settings → Change Source**

7. In the pop-up window, switch to **Advanced** mode

8. Modify the path:

   * Remove the full folder path from the first row
   * Keep only the file name in the second row

     ```
     \dim_customers.csv
     ```

9. In the first row:

   * Click the **ABC icon**
   * Change it to **Parameter**
   * Select `URL_FILES`

10. Click **OK**, then **Close & Apply**

---

### ⚠️ Important Notes

* Repeat the linking process for all tables:

  * `fact_inventory`
  * `fact_purchases`
  * `fact_returns`
  * `fact_sales`
  * `fact_support`
  * All dimension tables

* Ensure the `data/` folder contains all required CSV files before refreshing the report

---

## ⚠️ Attention

After downloading the files from GitHub, follow these steps to configure the data source:

1. Go to the **Home** tab in Power BI
2. Locate the **Base_URL** parameter
3. Update the **Current Value** with the new local path of your files
4. Press **Enter** to apply the changes
5. All the tables will be loaded
