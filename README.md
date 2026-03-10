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
