#  Retail Sales EDA Using SQL

A comprehensive Exploratory Data Analysis (EDA) of retail sales data using **SQL**. This project delves into sales trends, customer behavior, and product performance through structured queries and business-oriented insights.

---

##  Highlights

- Pure SQL-based data analysis—no external libraries required.
- Secured insights into sales trends, customer demographics, and top-performing products.
- Designed for data analysts looking to sharpen SQL problem-solving and query-building skills.

---

##  Dataset Overview

Uses a retail transaction dataset (`SQL - Retail Sales Analysis_utf .csv`) that likely includes:

- Transaction and customer IDs
- Sale dates/times
- Gender, age
- Product categories
- Quantity sold, unit price, total sale

*(Exact columns may vary; check your CSV.)*

---

##  SQL Schema & Structure

While your SQL schema isn't in a dedicated file, here’s a suggested structure you may have used:

```sql
CREATE TABLE retail_sales (
  transaction_id   INT PRIMARY KEY,
  sale_date        DATE,
  sale_time        TIME,
  customer_id      INT,
  gender           VARCHAR(10),
  age              INT,
  category         VARCHAR(50),
  quantity         INT,
  price_per_unit   DECIMAL(10,2),
  total_sale       DECIMAL(10,2)
);
```

---

##  Key Business Questions & Insights

Expected analysis categories include:

- **Sales Trends**: e.g., daily/monthly volume, peak hours.
- **Customer Demographics**: age/gender splits, high-value buyers.
- **Product Insights**: top categories, average price per category.
- **Performance Metrics**: total revenues, transaction counts, growth patterns.

*(Adjust based on the actual SQL queries in your `sql_query_p1.sql`.)*

---

##  Sample SQL Query

```sql
SELECT category,
       COUNT(*) AS total_transactions,
       SUM(total_sale) AS total_revenue
FROM retail_sales
GROUP BY category
ORDER BY total_revenue DESC;
```

---

##  Project File Breakdown

| File Name                    | Description                                   |
|-----------------------------|-----------------------------------------------|
| `SQL - Retail Sales Analysis_utf .csv` | Raw retail sales dataset            |
| `sql_query_p1.sql`          | SQL queries executing your EDA and insights    |
| `README.md`                 | This project overview                         |

---

##  How to Reproduce This Analysis

1. Clone the repository:
   ```bash
   git clone https://github.com/Priyanshupriyadarshi29/retail-sales-eda.git
   cd retail-sales-eda
   ```

2. Import the CSV into your SQL environment.

3. Run queries in `sql_query_p1.sql` against your `retail_sales` table.

4. Review outputs and insights generated via your SQL queries.

---

##  About Me

Hi! I'm **Priyanshu Priyadarshi**—a data enthusiast committed to deriving meaningful insights using SQL.

- **GitHub**: [@Priyanshupriyadarshi29](https://github.com/Priyanshupriyadarshi29)
