# 📖 Online BookStore Dataset Analysis

## 🔍 Overview

The **Online BookStore Dataset Analysis** project demonstrates efficient management and analysis of bookstore data using **PostgreSQL**. The project focuses on understanding book sales performance, customer behavior, and inventory insights through SQL queries and data analytics techniques.

---

## 📊 Key Features

* **Database Design & Management:**

  * Created and managed relational tables for **Books**, **Customers**, and **Orders**.
  * Ensured data integrity with proper relationships and constraints.

* **Data Analysis with SQL:**

  * Executed queries to retrieve key insights on stock levels, customer purchases, and total revenue.
  * Applied **JOINs**, **aggregate functions**, and **subqueries** for deep analytical insights.

* **Real-World Data Integration:**

  * Imported **CSV files** to simulate real bookstore transactions.
  * Conducted advanced analysis to identify:

    * 🌟 *Top-selling books*
    * 💼 *Most active customers*
    * 🔄 *Remaining stock updates*

---

## 📂 Dataset Details

The dataset includes multiple tables with the following schema highlights:

* **Books Table** – BookID, Title, Author, Genre, Price, Stock
* **Customers Table** – CustomerID, Name, Email, City
* **Orders Table** – OrderID, CustomerID, BookID, Quantity, OrderDate

---

## 👨‍💻 Tools & Technologies Used

* **Database:** PostgreSQL
* **Language:** SQL
* **Data Source:** CSV files
* **Environment:** pgAdmin / DBeaver / SQL Workbench

---

## 🔧 SQL Operations Performed

1. **Data Retrieval:** Extracted information about books, customers, and orders.
2. **Joins & Aggregations:** Combined datasets to calculate total revenue and customer spending.
3. **Stock Analysis:** Updated remaining stock after each purchase.
4. **Top Insights:** Ranked books and customers based on sales metrics.

---

## 🔖 Sample Queries

```sql
-- Retrieve top 5 selling books
SELECT b.title, SUM(o.quantity) AS total_sold
FROM orders o
JOIN books b ON o.bookid = b.bookid
GROUP BY b.title
ORDER BY total_sold DESC
LIMIT 5;

-- Calculate total revenue generated
SELECT SUM(o.quantity * b.price) AS total_revenue
FROM orders o
JOIN books b ON o.bookid = b.bookid;
```

---

## 💡 Insights Gained

* Identified **bestselling genres** and **high-revenue books**.
* Determined **customer buying patterns** and **location-based demand**.
* Improved **inventory forecasting** through stock and sales correlation.

---

## 🛍️ Future Enhancements

* Add **interactive Power BI dashboards** for better data visualization.
* Implement **stored procedures** for automated updates and reporting.
* Integrate **machine learning** for predicting future book demand.

---

## 📦 Repository Structure

```
Online-BookStore-Dataset-Analysis/
│
├── Books.csv
├── Customers.csv
├── Orders.csv
├── Queries.sql
└── README.md
```

---

## 📙 Author

**Manasi Patil**
Data Analyst | UI/UX Enthusiast | Python & SQL Developer

---

## 📢 Connect With Me

* 💼 [LinkedIn](https://www.linkedin.com/in/manasi-patil)
* 🐙 [GitHub](https://github.com/ManasiPatil123)

---

> "Turning raw data into meaningful insights for smarter decisions."
