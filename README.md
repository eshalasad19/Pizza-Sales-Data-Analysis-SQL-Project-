# 🍕 Pizza Sales Data Analysis (SQL Project)

### 📌 Overview  
This project explores pizza sales data using SQL to uncover business insights about performance, trends, and revenue.  
It demonstrates how SQL can be used to answer real-world business questions — from calculating total revenue to identifying best-selling pizzas and analyzing time-based order patterns.

---

### 🎯 Objectives  
- Calculate total revenue and total number of orders  
- Identify top-selling pizzas and most popular pizza sizes  
- Analyze hourly, daily, and category-wise sales  
- Find the percentage contribution of each pizza category  
- Track cumulative revenue growth over time  

---

### 🧠 Key Insights Generated  
- **Total Orders:** Counted using `COUNT()`  
- **Highest Priced Pizza:** Found using `MAX()`  
- **Total Revenue:** `SUM(price × quantity)`  
- **Most Common Pizza Size:** Grouped and ranked by size  
- **Top 5 Pizza Types:** Sorted by total quantity sold  
- **Category-wise Distribution:** `GROUP BY category`  
- **Hourly Sales Trend:** `HOUR(order_time)` grouping  
- **Average Pizzas per Day:** Subquery + `AVG()`  
- **Revenue Contribution:** Calculated as a percentage of total sales  
- **Cumulative Revenue:** Using SQL window function `OVER(ORDER BY ...)`  

---

### 🧩 Database Structure  
**Database Name:** `pizza_sales`  

**Tables Used:**  
| Table Name | Description |
|-------------|-------------|
| `orders` | Order ID, date, and time of order |
| `order_details` | Pizza ID, order ID, quantity ordered |
| `pizzas` | Pizza details such as size, type ID, and price |
| `pizza_types` | Pizza name, category, and ingredients |

---

### ⚙️ How to Import the Data  

#### 🧾 Step 1: Create the Database  
```sql
CREATE DATABASE pizza_sales;
USE pizza_sales;

#### 🧾 Step 2: Import Tables
#### Option 1: Using phpMyAdmin
Open phpMyAdmin from XAMPP.

Click on Databases → Create new database → pizza_sales.

After creating it, click on the database name.

Go to the Import tab.

Click Choose File → Select the SQL or CSV file for each table (orders, order_details, pizzas, pizza_types).

Click Go to import the data.

Repeat for all tables if importing separately.

#### Option 2: Using MySQL Workbench
Open MySQL Workbench.

Connect to your local MySQL server.

Run the following command:

sql
Copy code
CREATE DATABASE pizza_sales;
USE pizza_sales;
Go to Server → Data Import.

Choose Import from Self-Contained File and select your .sql file (like pizza_sales.sql).

Select the target schema as pizza_sales.

Click Start Import.

After import, open a new query tab and run your SQL queries.

#### 🧰 Tools & Technologies
MySQL / phpMyAdmin

MySQL Workbench

SQL Queries (Joins, Subqueries, Aggregate & Window Functions)
