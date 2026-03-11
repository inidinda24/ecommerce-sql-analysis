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

