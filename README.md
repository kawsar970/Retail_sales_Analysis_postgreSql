# Retail_sales_Analysis_postgreSql
Retail Sales Analysis Using PostgreSQL
Project Overview
This project uses PostgreSQL to explore retail transaction data and
answer business questions about sales performance, product categories,
customer purchasing patterns, and order timing. The SQL script creates a
retail_sales table, checks for missing values, removes rows containing
nulls in the listed fields, and runs ten analysis queries.
Project Objectives
- Prepare a retail sales table for analysis.
- Identify and remove records with missing values in required columns.
- Summarize revenue and transaction volume by product category.
- Examine customer demographics and purchasing behavior.
- Compare sales across years and months.
- Identify high-value customers and transactions.
- Understand how order volume varies by time of day.
Tools Used
- PostgreSQL --- relational database and SQL analysis.
- SQL --- table creation, data quality checks, filtering,
  aggregation, and analytical queries.
Dataset Description
The SQL script defines a table named retail_sales with the following
columns:

  Column             SQL data type   Description supported by the schema
  transaction_id   INT           Transaction identifier; primary key
sale_date        DATE          Date of the sale
sale_time        TIME          Time of the sale
customer_id      INT           Customer identifier
gender           VARCHAR(15)   Customer gender value
age              INT           Customer age
category         VARCHAR(15)   Product category
price_per_unit   FLOAT         Price per unit
quantity         INT           Quantity sold
cogs             FLOAT         Cost of goods sold
total_sale       FLOAT         Total sale amount for the transaction

The script defines the table structure but does not include the source
dataset, insert/load statements, or query-result outputs. Therefore,
record counts, date coverage, category values, and numerical findings
cannot be confirmed from this SQL file alone.
Data Cleaning and Preparation
The script performs the following preparation steps:
1. Drops retail_sales if it already exists, then creates it with the
   columns listed above.
2. Uses SELECT * to inspect the table.
3. Checks for null values in the transaction ID, date, time, customer
   ID, gender, age, category, quantity, unit price, cost of goods sold,
   and total sale fields.
4. Deletes rows where any of those fields is null.
5. Selects the table again after the deletion.
The script does not show additional cleaning procedures such as
duplicate detection beyond the primary-key constraint, outlier
treatment, value standardization, or validation of business rules.
SQL Concepts Demonstrated
- DDL: DROP TABLE IF EXISTS and CREATE TABLE.
- Constraints: Primary key on transaction_id.
- Data quality checks: IS NULL conditions and DELETE.
- Filtering: WHERE, comparison operators, AND, and date
  conditions with BETWEEN.
- Sorting and limiting: ORDER BY and LIMIT.
- Aggregation: SUM, COUNT, COUNT(DISTINCT ...), and AVG.
- Grouping: GROUP BY across one or more dimensions.
- Date analysis: EXTRACT(YEAR ...) and EXTRACT(MONTH ...).
- Conditional logic: CASE expressions for time-of-day shifts.
- CTEs: WITH clause to organize monthly sales calculations.
- Window functions: RANK() with PARTITION BY to rank months
  within each year.
Business Questions
The project script contains these ten analysis questions:
1. Sales on a specific date: Retrieve all columns for transactions
   dated November 5, 2022.
2. Clothing transactions in November: Retrieve Clothing
   transactions with quantity greater than 2 during the specified date
   range.
3. Category performance: Calculate total sales revenue and
   transaction count for each product category.
4. Beauty customer age: Calculate the average age of customers who
   purchased from the Beauty category.
5. High-value transactions: Retrieve transactions with a total sale
   of at least 1,000 and sort them by sale amount.
6. Gender and category breakdown: Count transactions for each
   gender within each product category.
7. Best-selling month by year: Calculate monthly sales totals and
   rank the months within each year, returning the top-ranked month or
   months.
8. Top five customers: Rank customers by summed total sales and
   return the five highest.
9. Unique customers by category: Count distinct customers who
   purchased from each category and sort categories by that count.
10. Orders by time-of-day shift: Classify orders as Morning,
    Afternoon, or Evening and count orders in each shift:
    - Morning: before 12:00 PM
    - Afternoon: 12:00 PM to before 6:00 PM
    - Evening: 6:00 PM onward
Key Findings
The supplied SQL file contains the analysis queries but does not contain
their result sets or the underlying transaction records. As a result, it
does not support reporting specific figures or conclusions such as the
highest-revenue category, best-performing month, top customer, average
Beauty customer age, or busiest shift.

The queries are designed to reveal:
- Revenue and transaction volume by category.
- Customer age and gender patterns across categories.
- Monthly sales peaks by year.
- Customers contributing the highest total sales.
- Category reach measured by distinct customers.
- Order distribution across Morning, Afternoon, and Evening shifts.
Populate this section with verified values after running the queries
against the project dataset.
Business Value
The analysis framework can help a retail business:
- Compare product categories by revenue and transaction count.
- Understand customer mix across product categories.
- Identify high-value customers for retention and engagement efforts.
- Recognize stronger sales months to inform planning.
- Review transaction values and order volumes across the day.
- Use data-quality checks to reduce the impact of incomplete records
  on analysis.
These are potential uses of the analysis; the SQL file does not provide
evidence of implemented business actions or measured business outcomes.
Conclusion
This project demonstrates a PostgreSQL workflow for preparing a retail
sales table and answering ten business-focused questions using
filtering, aggregation, date functions, CTEs, window functions, and
conditional logic. It provides a foundation for examining sales
performance, customer behavior, and order timing. Numerical findings
should be added only after executing the queries against the actual
dataset and validating the returned results.

--Author 
kawsar Ahmad Anik
