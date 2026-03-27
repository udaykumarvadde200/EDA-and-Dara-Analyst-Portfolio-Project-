# EDA-and-Data-Analyst-Portfolio-Project-
# SQL Data Analytics Project

## Overview

This project demonstrates how SQL can be used to perform end-to-end **data analytics** on structured sales data. It includes database creation, schema design, CSV-based data loading, exploratory analysis, business metric calculations, time-based trend analysis, segmentation, and final customer/product reporting views.

The project is built in **SQL Server** using **T-SQL** and focuses on extracting meaningful insights from sales, customer, and product data.

---

## Project Objectives

* Build a structured analytics database in SQL Server
* Load customer, product, and sales data from CSV files
* Explore and validate the dataset
* Calculate important business KPIs
* Analyze trends over time
* Segment customers and products
* Create reusable SQL views for reporting

---

## Database Structure

The project uses a `gold` schema with the following tables:

### 1. `gold.dim_customers`

Contains customer-related information such as:

* customer ID
* customer number
* first name
* last name
* country
* marital status
* gender
* birthdate
* create date

### 2. `gold.dim_products`

Contains product-related information such as:

* product ID
* product number
* product name
* category
* subcategory
* maintenance
* cost
* product line
* start date

### 3. `gold.fact_sales`

Contains transactional sales data such as:

* order number
* product key
* customer key
* order date
* shipping date
* due date
* sales amount
* quantity
* price

---

## Key Features

* Database creation and schema setup
* Data loading using `BULK INSERT`
* Database and table exploration using `INFORMATION_SCHEMA`
* Dimension exploration for categories, products, and countries
* Date range analysis for orders and customers
* KPI calculations such as:

  * total sales
  * total quantity
  * average price
  * total orders
  * total customers
  * total products
* Magnitude analysis across:

  * countries
  * gender
  * product categories
  * customer revenue
* Performance analysis using:

  * `LAG()`
  * `AVG() OVER()`
  * year-over-year comparisons
* Change-over-time analysis using:

  * `YEAR()`
  * `MONTH()`
  * `DATETRUNC()`
  * `FORMAT()`
* Cumulative analysis using window functions
* Customer segmentation based on spending and lifespan
* Product segmentation based on revenue
* Part-to-whole contribution analysis
* Reporting views for customer and product analytics

---

## Types of Analysis Performed

### 1. Database Exploration

The project explores the schema and metadata using:

* `INFORMATION_SCHEMA.TABLES`
* `INFORMATION_SCHEMA.COLUMNS`

### 2. Dimension Exploration

The project identifies:

* unique customer countries
* product categories
* subcategories
* product names

### 3. Date Range Exploration

The project analyzes:

* first and last order dates
* total order range in months
* oldest and youngest customers

### 4. Measures Exploration

The project calculates overall business metrics such as:

* total sales
* total quantity sold
* average selling price
* total number of orders
* total products
* total customers

### 5. Magnitude Analysis

The project groups data to measure:

* customers by country
* customers by gender
* products by category
* average cost by category
* revenue by category
* revenue by customer

### 6. Performance Analysis

The project compares yearly product sales against:

* previous year sales
* average product sales
* yearly increase/decrease trends

### 7. Change Over Time Analysis

The project tracks sales trends over time using:

* monthly sales summaries
* yearly summaries
* customer activity by month

### 8. Cumulative Analysis

The project calculates:

* running total sales
* moving average price

### 9. Segmentation Analysis

The project segments:

* products by cost range
* customers by spending behavior:

  * VIP
  * Regular
  * New

### 10. Part-to-Whole Analysis

The project calculates how much each category contributes to overall sales.

---

## Reporting Views

### `gold.report_customers`

This view creates a customer-level analytical report including:

* customer name
* age
* age group
* customer segment
* last order date
* recency
* total orders
* total sales
* total quantity
* total products
* lifespan
* average order value
* average monthly spend

### `gold.report_products`

This view creates a product-level analytical report including:

* product name
* category
* subcategory
* cost
* last sale date
* recency in months
* product segment
* lifespan
* total orders
* total sales
* total quantity
* total customers
* average selling price
* average order revenue
* average monthly revenue

---

## Technologies Used

* SQL Server
* T-SQL
* Window Functions
* Aggregate Functions
* CTEs
* Views
* BULK INSERT
* CSV files

---

## SQL Concepts Used

This project uses a wide range of SQL concepts, including:

* `SELECT`
* `WHERE`
* `GROUP BY`
* `ORDER BY`
* `JOIN`
* `DISTINCT`
* `COUNT()`
* `SUM()`
* `AVG()`
* `MIN()`
* `MAX()`
* `DATEDIFF()`
* `CASE`
* `CTE`
* `UNION ALL`
* `LAG()`
* `SUM() OVER()`
* `AVG() OVER()`
* `ROUND()`
* `FORMAT()`
* `DATETRUNC()`
* `CREATE VIEW`

---

## Project Workflow

1. Create the `DataWarehouseAnalytics` database
2. Create the `gold` schema
3. Create dimension and fact tables
4. Load CSV files into SQL Server using `BULK INSERT`
5. Explore and validate the loaded data
6. Perform descriptive and analytical SQL queries
7. Build reusable reporting views for customers and products

---

## Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/vaddeudaykumar200/sql-data-analytics-project.git
```

### 2. Open SQL Server Management Studio

Run the SQL scripts in sequence.

### 3. Update file paths

Before running `BULK INSERT`, update the CSV paths to match your system.

Example:

```sql
FROM 'C:\Users\uday kumar\Desktop\GATE DA 26\SQL project\Project2\sql-data-analytics-project-main\sql-data-analytics-project-main\datasets\csv-files\gold.dim_customers.csv'
```

### 4. Execute scripts

Run:

* database creation script
* table creation script
* data loading script
* analytics queries
* report view creation script

---

## Business Insights Supported by This Project

This project helps answer questions like:

* What are the total sales of the business?
* Which product categories generate the most revenue?
* Which customers bring the highest revenue?
* How do sales change over time?
* Which products are high performers?
* Which customers are VIPs?
* Which categories contribute the most to total sales?

---

## Learning Outcomes

Through this project, I gained hands-on experience in:

* designing structured analytics databases
* loading external data into SQL Server
* performing exploratory data analysis with SQL
* writing complex analytical queries
* using window functions for trend analysis
* building reporting views for business decision-making

---

## Future Improvements

* Add stored procedures for automated data loading
* Add data quality checks before analysis
* Build a Power BI dashboard on top of the reporting views
* Add indexes for performance optimization
* Include ER diagram / schema image in the repository

---

## Author

**Uday Kumar**
B.Tech (ECE), RGUKT RK Valley

GitHub: [vaddeudaykumar200](https://github.com/vaddeudaykumar200)

---

## Repository Link

[SQL Data Analytics Project](https://github.com/vaddeudaykumar200/sql-data-analytics-project)
