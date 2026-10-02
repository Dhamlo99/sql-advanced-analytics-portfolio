# 🍫 Awesome Chocolates: Global Sales & Performance Analysis

## 📌 Project Overview
This project analyzes the global sales performance, product profitability, and workforce efficiency of "Awesome Chocolates." Using a dataset of over 300 individual sales records across multiple geographic regions, this analysis answers critical business questions ranging from basic revenue aggregations to complex salesperson performance rankings.

The objective of this repository is to demonstrate advanced SQL querying techniques to extract actionable business intelligence regarding product costs, regional sales dominance, and individual team member performance.

## 🗄️ Database Architecture
The analysis is built on a relational database consisting of four primary tables. 

| Table | Description | Key Fields |
| :--- | :--- | :--- |
| `sales` | Transactional records of chocolate sales | `SPID`, `GeoID`, `PID`, `Amount`, `Customers`, `Boxes` |
| `people` | Sales team directory and locations | `SPID`, `Salesperson`, `Team`, `Location` |
| `products`| Chocolate portfolio dimensions and costs | `PID`, `Product`, `Category`, `Cost_per_box` |
| `geo` | Geographic territory mappings | `GeoID`, `Geo`, `Region` |

*Note: View the visual Entity-Relationship Diagram in `awesome_chocolates_ERD.png`.*

## 🛠️ Tech Stack & SQL Concepts Demonstrated
*   **Dialect:** MySQL
*   **Core Concepts:** Multi-table `JOIN`s, Aggregations (`SUM`, `AVG`, `COUNT`), `GROUP BY` & `HAVING` clauses.
*   **Advanced Concepts:** 
    *   Common Table Expressions (CTEs) for multi-step logic.
    *   Window Functions (`DENSE_RANK()`, `PARTITION BY`) for regional and category-specific leaderboards.
    *   Conditional Logic (`CASE WHEN`) for dynamic performance classification.
    *   Safe Arithmetic (`NULLIF`) for accurate Revenue-per-Box calculations.

## 📊 Key Business Inquiries Addressed
This analysis progresses from exploratory data cleaning to advanced reporting, answering 20 distinct business inquiries including:

1.  **Cost & Profitability:** Calculating the estimated product cost and revenue generated per box for every product in the portfolio to identify the highest-margin items.
2.  **Regional Dominance:** Identifying the top 3 performing salespeople strictly within their assigned geographic regions using windowed rankings.
3.  **Workforce Classification:** Dynamically segmenting the sales force into "Excellent," "Good," and "Needs Improvement" tiers based on lifetime revenue generation.
4.  **High-Value Categories:** Isolating product categories where the average transaction amount consistently exceeds $8,000.

## 📁 Repository Navigation
*   `/data`: Contains the `awesome chocolates.sql` setup script to recreate the schema and populate the tables.
*   `/queries`: Contains the `.sql` scripts used for the analysis, categorized by complexity and business function.
