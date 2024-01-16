#  Sales-Analysis-and-Visualization
## Overview

This repository contains Tableau visualizations created for a computer hardware company using approximately 150,000 transaction records. The data was explored in SQL Server to identify key performance indicators (KPIs), and two dashboards were developed in Tableau. The first dashboard focuses on revenue analysis, while the second one centers around profit analysis.

## Tableau Dashboards
### Revenue Analysis Dashboard

Provides insights into revenue trends over the specified time frame.
Includes visualizations for product-wise revenue distribution.
Highlights key factors influencing revenue, such as top-selling products and revenue by region.
Offers interactive features for users to drill down into specific details.

### Profit Analysis Dashboard

Offers a comprehensive view of profit margins and trends.
Visualizes profit contributions from different product categories.
Identifies factors affecting profit, including profit by customer segments and profit margin by region.
Enables users to dynamically explore profit-related insights.

## Data Exploration
The data was initially explored in SQL Server to understand its structure and identify relevant KPIs.
SQL queries used for data exploration are provided here.

1.Show all customer records

SELECT * FROM customers;

2.Show total number of customers

SELECT count(*) FROM customers;

3.Show transactions for Chennai market (market code for chennai is Mark001

SELECT * FROM transactions where market_code='Mark001';

4.Show distrinct product codes that were sold in chennai

SELECT distinct product_code FROM transactions where market_code='Mark001';

5.Show transactions where currency is US dollars

SELECT * from transactions where currency="USD"

6.Show transactions in 2020 join by date table

SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;

7.Show total revenue in year 2020,

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";

8.Show total revenue in year 2020, January Month,

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");

9.Show total revenue in year 2020 in Chennai

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";

## Sales Analysis.twb for profit and revenue related visualizations. or use Tableau link 

https://public.tableau.com/views/SalesAnalysis_17053884965290/RevenueAnalysis?:language=en-US&:display_count=n&:origin=viz_share_link

Explore the dashboards interactively and gain valuable insights.

## Requirements

Tableau Desktop or Tableau Public for visualization exploration.
SQL Server for data exploration and extraction.

