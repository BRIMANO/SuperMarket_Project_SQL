# Supermarket Sales SQL Analysis Project

## 📄 Project Overview
This project involves a comprehensive **Exploratory Data Analysis (EDA)** of a supermarket's sales data using Structured Query Language (SQL). The goal is to derive actionable insights regarding customer demographics, purchasing behaviors, branch performance, and product profitability.

The project utilizes a dataset containing **transaction records** from three different branches (New York, Los Angeles, Chicago) to answer key business questions and identify trends.

## 📊 Database Schema
The analysis is based on a single table named `sales_record`. Below is the structure of the dataset:

| Column Name | Data Type | Description |
| :--- | :--- | :--- |
| `sale_id` | `INT` | Unique identifier for each transaction |
| `branch` | `VARCHAR(1)` | Branch identifier (e.g., A, B) |
| `city` | `VARCHAR(11)` | Location of the store (New York, Los Angeles, Chicago) |
| `customer_type` | `VARCHAR(6)` | Type of customer (Member vs. Normal) |
| `gender` | `VARCHAR(6)` | Gender of the customer |
| `product_name` | `VARCHAR(12)` | Name of the item sold |
| `product_category`| `VARCHAR(13)` | Category (e.g., Fruits, Personal Care, Household) |
| `unit_price` | `NUMERIC(4, 2)`| Price per single unit |
| `quantity` | `INT` | Number of units purchased |
| `tax` | `NUMERIC(4, 2)`| Tax amount calculated on the sale |
| `total_price` | `NUMERIC(5, 2)`| Final transaction value including tax |
| `reward_points` | `INT` | Points awarded for the transaction |

## 🛠️ Key Analysis & Objectives
The SQL script performs several distinct analyses to evaluate business performance. The project includes detailed financial, loyalty, and demographic metrics.

### 1. Product Performance & Profitability
* **Top Selling Products:** Identifies the top 10 specific products based on the total quantity sold and revenue generated.
* **Category Profitability:** Calculates the net profit per category by subtracting tax from the total price (`total_price - tax`).
* **Tax Contribution:** Analyzes which product categories contribute the most to the overall tax liability of the business.

### 2. Customer Loyalty & Demographics
* **Reward Points Analysis:** Evaluates which product categories are driving the most customer engagement by summing up reward points.
* **Customer Segmentation:** Analysis of spending habits based on `customer_type` (Member vs. Normal) and `gender`.
* **Spending Power:** Comparing average transaction values between men and women, and members versus non-members.

### 3. Branch & Regional Insights
* **Category Popularity by Branch:** A granular view of which product categories sell the highest volume at specific branch locations (A vs. B).
* **Revenue by Location:** Ranking cities (Chicago, New York, Los Angeles) by total revenue.
* **Footfall Analysis:** Counting unique customer transactions per city to determine the busiest locations.

### 4. Operational KPIs
High-level metrics to gauge overall business health:
* Average Unit Price
* Total Quantity Sold
* Total Revenue Generated
* Tax collected per category

## 💡 Key Findings
Based on the analysis executed in the SQL script, the following insights were observed:

* **Top Performing City:** **Chicago** leads in revenue ($85,169), closely followed by New York.
* **Lowest Performing City:** **Los Angeles** generated the lowest revenue ($71,545).
* **Branch Dominance:** **Branch A** significantly outperformed Branch B, generating over double the transaction volume.
* **Pricing Strategy:** The average unit price is **$10.84**, suggesting a strategy focused on moderately priced goods.
* **Product Insights:** The analysis allows the business to identify specific categories (e.g., *Household* vs *Personal Care*) that yield higher tax returns versus those that drive high reward point accumulation.
* **Sales Volume:** A total of **20,674** units were sold, indicating strong market demand.

## 🚀 How to Run This Project

1.  **Prerequisites:** You need an SQL database management system installed (e.g., PostgreSQL, MySQL, or SQL Server).
2.  **Setup:**
    * Open your SQL Query Editor.
    * Copy the content of the `Customer_Demographics.sql` file.
3.  **Execution:**
    * Run the `CREATE TABLE` and `INSERT INTO` statements first to populate the database with the 1,000 records.
    * Execute the `SELECT` statements individually to view specific insights.
To do list
