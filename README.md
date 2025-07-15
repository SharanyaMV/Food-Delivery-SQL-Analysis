# Food-Delivery-SQL-Analysis
Project Overview
This project focuses on analyzing a food delivery database using SQL queries. The goal is to extract insights, identify data inconsistencies, and optimize delivery logistics.

Objective
 Retrieve customer and order details from the database 
 Identify peak order times for better resource management 
 Optimize delivery efficiency by sorting orders by apartment floor 
 Detect missing data and resolve inconsistencies

Database Schema
The dataset consists of the following columns:

order_id (INT) – Unique order identifier

order_time (DOUBLE) – Time order was placed

customer_id (VARCHAR) – Unique customer identifier

customer_name (VARCHAR) – Name of the customer

address_pincode (INT) – Delivery pincode

apartment_floor (INT) – Floor number of the apartment

Key SQL Queries & Results

1️⃣ Retrieve Sample Data (First 3 Entries)

SELECT * FROM Orders

LIMIT 3;

2️⃣ Extract Unique Delivery Pincodes

SELECT DISTINCT address_pincode FROM Orders;

3️⃣ Identify Orders Placed Between 12 PM and 1 PM

SELECT * FROM Orders

WHERE order_time BETWEEN 12 AND 13;

4️⃣ Retrieve Customers Whose Name Ends with ‘a’

SELECT DISTINCT customer_id FROM Orders

WHERE customer_name LIKE '%a';

5️⃣ Optimize Delivery by Sorting Orders by Floor

SELECT * FROM Orders

ORDER BY apartment_floor;

6️⃣ Identify Orders with Missing Order Time

SELECT order_id FROM Orders

WHERE order_time IS NULL;

7️⃣ Correct Query for Filtering Specific Customers

SELECT DISTINCT customer_name

FROM Orders

WHERE (address_pincode = 122001 OR address_pincode = 122002)

AND order_time < 12.30

AND apartment_floor >= 3;

Skills Demonstrated
SQL Proficiency: Querying, filtering, sorting, and data cleaning
Data Analysis: Extracting meaningful insights from structured datasets 
Problem-Solving: Optimizing delivery logistics and identifying data issues

Tech Stack
SQL (Queries, Filtering, Sorting, and Data Cleaning)
