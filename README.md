

# 🚀 **Advanced SQL Data Analytics Portfolio Project**

## **Project Overview**

Welcome to the **Advanced SQL Data Analytics Portfolio Project**! This repository showcases real-life data analytics skills using **Advanced SQL techniques**. Led by Baraa, a Big Data project lead in major companies, this project goes beyond theory to provide **practical, real-world experience**.

The main goal of this project is to demonstrate how to **solve real business questions** by performing various types of advanced analyses on datasets and generating insightful reports. By completing this project, you will be well-equipped to **analyze any dataset in any domain**.

## **Key Learning & Techniques**

This project covers the "Advanced analytics projects" type of SQL data analytics, focusing on **complex SQL queries**. You will learn to apply:

*   **Advanced Window Functions**.
*   **Common Table Expressions (CTEs)**.
*   **Subqueries**.

Through these techniques, the project addresses crucial business analysis needs:

*   **Tracking Changes Over Time (Time-series Analysis)**: Analyzing how measures evolve over time to track trends and identify seasonality (e.g., total sales by year, average cost by month).
*   **Cumulative Analysis**: Aggregating data progressively over time to understand business growth or decline (e.g., running total of sales, moving average of sales).
*   **Performance Analysis**: Comparing current values against target values (like averages or previous periods) to measure success and identify high/low performers (e.g., comparing current year sales with previous year sales).
*   **Part-to-Whole Analysis**: Determining the proportion of a part relative to the whole to understand the contribution of individual categories (e.g., percentage of total sales contributed by a product category).
*   **Data Segmentation**: Grouping data based on specific ranges to create new categories and derive insights (e.g., segmenting products into cost ranges, grouping customers by spending behavior).

## **Project Setup and Data**

To follow along with this project, you will need:

*   **SQL Server & SQL Server Management Studio (SSMS)**: Links to download these tools are provided.
*   **Project Files**: All necessary scripts and datasets are available for download.

There are **three recommended ways to set up the database** for this project:

1.  **Executing SQL Scripts (Recommended)**: Copy and execute the `init_database.sql` script. Remember to adjust the file path within the script. This method creates a new database, schema, and three essential tables: `Customer`, `Product`, and `Sales`.
2.  **Importing Flat Files**: Create a new database in SSMS, then use the "Import Flat File" task to import the provided CSV files for `Customer`, `Product`, and `Sales`.
3.  **Restoring Database Backup**: Copy the provided `.bak` file to your SQL Server backup location and then restore the database via SSMS.

*(Note: If you have previously built the SQL data warehouse project with "Data with Baraa", you might already have the necessary data and database set up).*

## **Project Roadmap & Structure**

The project follows a structured roadmap, progressing through different analytical steps and culminating in the creation of comprehensive reports. This often involves a multi-step CTE approach:

1.  **Base Data CTE (`base_query`)**: Initial selection of relevant columns from joined fact and dimension tables, along with basic data transformations (e.g., concatenating names, calculating age) and filtering (e.g., removing nulls). This establishes the scope for subsequent analyses.
2.  **Aggregations CTE (`customer_aggregation` / `product_aggregation`)**: Performing necessary aggregations on the base data, such as `SUM` for total sales, `COUNT DISTINCT` for total orders, and calculating measures like `lifespan` and `last_order_date`.
3.  **Final Results CTE**: Bringing together all the aggregated data, applying final transformations, and generating key performance indicators (KPIs) and data segments.
    *   **KPIs calculated**: Recency (months since last order), Average Order Value (AOV), Average Monthly Spend.
    *   **Data Segmentation**: Using `CASE WHEN` statements to create new categories (e.g., customer segments like VIP, Regular, New; age groups; product revenue segments).

## **Deliverables & Impact**

The ultimate output of this project is the creation of **two solid, amazing reports** in the form of **SQL Views** within the database:

1.  **`gold.report_customers`**: A comprehensive, 360-degree view of customers, consolidating key metrics, behaviors, demographic details, and segments (VIP, Regular, New customers; Age Groups).
2.  **`gold.report_products`**: A detailed report on products, including details, categories, subcategories, costs, and segments (High, Medium, Low revenue performers).

These views are designed to be readily consumable by other data analysts or stakeholders. They can be connected to **visualization tools like Tableau or PowerBI** or queried directly using SQL to **quickly generate insights** and support strategic decision-making without needing to perform extensive data preparation.

## **Repository Best Practices**

As recommended, this repository will include:

*   **Data Sets**: The raw data used for the project.
*   **Documentation**: Explanations of the project and its methodologies.
*   **Scripts**: All the SQL queries developed throughout the project, meticulously organized.
*   **Clean Code**: Emphasizing **nice commenting**, **formatting**, and **styling** to ensure readability and maintainability.

---
