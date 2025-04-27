# Oracle Views and Materialized Views Performance Study

## Description
This project focuses on understanding the importance and practical use of **Views** and **Materialized Views** to optimize query performance in Oracle databases.  
It simulates a large-scale database environment to analyze how different types of views can affect query speed and resource usage.

## 🛠Technologies Used
- Oracle SQL
- PL/SQL
- DBMS_RANDOM
- DBMS_XPLAN

## Project Objectives
- Create large datasets (millions of rows) to simulate real-world database sizes.
- Implement simple Views and Materialized Views (both Build Immediate and Build Deferred).
- Measure and compare query execution times across normal queries, Views, and Materialized Views.
- Understand the performance impact and refresh strategies of Materialized Views.

## Project Structure
- **Tables Creation**: `products`, `orders`, `stock_movements`.
- **Data Insertion**: Use PL/SQL anonymous blocks with loops to generate millions of random records.
- **Views**:
  - Simple View (`S_VIEW`)
  - Materialized View Build Immediate (`MBI_VIEW`)
  - Materialized View Build Deferred (`MBD_VIEW`)
- **Performance Analysis**:
  - Query Execution Time using `SET TIMING ON`.
  - Query Plan Analysis using `EXPLAIN PLAN` and `DBMS_XPLAN.DISPLAY`.

## 🚀 How to Run
1. Execute the SQL scripts in an Oracle environment (SQL*Plus, SQL Developer, or any Oracle client).
2. Make sure you have sufficient resources (RAM, disk space) for handling large datasets.
3. Use `SET TIMING ON` to measure query execution time.
4. Refresh Materialized Views manually using:
   ```sql
   EXEC DBMS_MVIEW.REFRESH('MBI_VIEW');
   EXEC DBMS_MVIEW.REFRESH('MBD_VIEW');
