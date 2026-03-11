# ecommerce-sql-analysis
SQL-based analysis of an e-commerce dataset to uncover sales performance and customer insights.

## Project Structure
The repository is organized as follows:
- dataset: contains the raw CSV files used for the analysis
- sql_queries: contains SQL scripts used during the analysis
- README.md: project documentation

## Database Setup
The dataset is stored in a PostgreSQL database consisting of four relational tables:
- customers
- products
- orders
- order_items
These tables simulate a simplified e-commerce transactional database.
Relationships between tables:
customers → orders → order_items → products
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f78bf0d2-5e69-4a4b-aab9-426cbb6fbf50" />

## Importing Dataset into PostgreSQL
The dataset used in this project consists of four CSV files representing an e-commerce transactional system. These files were imported into a PostgreSQL database using pgAdmin.

The following tables were created in the database:
- customers
- products
- orders
- order_items

Each CSV file corresponds to one table in the relational database.

### Import Process
1. A new PostgreSQL database named `ecommerce_analysis` was created.
2. Tables were created using SQL scripts in the Query Tool.
3. The CSV datasets were imported using the **Import/Export Data** feature in pgAdmin.
4. During the import process, the correct delimiter (`,`) and header options were specified to ensure proper column mapping.

### Data Validation
After importing the data, validation queries were executed to confirm that the data had been successfully loaded into each table. Sample queries such as `SELECT * FROM table_name LIMIT 10;` were used to preview the imported records.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/de1de3cf-ee40-4e48-b218-8f97a643f03b" />

## SQL Analysis for Business Insight

## Revenue Overview

The first analysis calculates the total revenue generated from all transactions in the dataset.

Revenue is calculated by multiplying the quantity of each item sold with its product price. The order_items table is joined with the products table to retrieve pricing information.

This metric provides a high-level overview of the overall business performance.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/43c1a17e-948a-4642-9bc7-80b0478868bf" />

## Monthly Sales Trend

This analysis examines the sales performance over time by aggregating revenue on a monthly basis.

The DATE_TRUNC function is used to group transactions by month. This allows us to identify sales trends and patterns throughout the year.

Understanding monthly sales trends helps businesses monitor growth, detect seasonal patterns, and evaluate overall performance.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/557ada26-9be4-4707-92cd-2e7f51a333e0" />

## Top Selling Products

This query identifies the best-selling products based on total units sold.

By aggregating the quantity column in the order_items table and joining it with the products table, we can determine which products are the most popular among customers.

These insights can help businesses optimize inventory management and marketing strategies.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c07ca966-3e76-46dc-873e-9b0a77c6fb9b" />

## Revenue by Product Category

This analysis evaluates revenue contribution by product category.

By grouping the total sales by category, businesses can identify which product segments generate the highest revenue.

This information is valuable for strategic decision-making such as product development, marketing investment, and inventory prioritization.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e74d281a-85f4-4faf-a862-1a35842c0926" />

## Top Customers by Revenue

This analysis identifies the customers who contribute the most revenue to the business.

By joining customers, orders, order_items, and products tables, the total spending of each customer can be calculated.

Recognizing high-value customers allows businesses to implement targeted retention strategies and loyalty programs.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/41a9d3ec-a9dc-4606-82aa-f219eb8c6f04" />

## Data Visualization with Power BI

After completing the SQL analysis in PostgreSQL, the resulting dataset was exported and used to build an interactive dashboard in Power BI.
The purpose of the dashboard is to transform raw SQL query results into visual insights that can help stakeholders understand business performance more easily.

### Data Preparation
A consolidated dataset was created using SQL by joining the following tables:
- customers
- orders
- order_items
- products

The query combined transaction data with product and customer information to produce a dataset containing:
- order information
- customer details
- product details
- quantity and price
- calculated revenue

This dataset was exported as a CSV file and imported into Power BI for visualization.

### Dashboard Metrics
Several key metrics were created to evaluate business performance:
- Total Revenue
- Total Orders
- Total Customers

These KPIs provide a high-level overview of the overall sales performance.

### Dashboard Visualizations
The Power BI dashboard includes the following visualizations:

**1. Monthly Revenue Trend**
A line chart showing how revenue changes over time. This helps identify sales trends and seasonal patterns.

**2. Top Selling Products**
A bar chart displaying the products with the highest number of units sold.

**3. Revenue by Product Category**
This visualization highlights which product categories contribute the most to total revenue.

**4. Top Customers by Revenue**
A chart showing the customers who generate the highest revenue for the business.

### Interactive Filters
Slicers were added to allow users to filter the dashboard by:
- Country
- Product Category
- Order Date

These filters enable interactive exploration of the data and provide deeper insights into sales performance across different segments.

### Dashboard Preview
Below is a preview of the Power BI dashboard created for this project.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/41af6457-f81f-49f6-91d2-bcb7688405ac" />



