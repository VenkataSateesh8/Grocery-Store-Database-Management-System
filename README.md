# Grocery Store Database Management System

A comprehensive SQL database system for managing grocery store operations, including customer orders, product inventory, supplier management, and sales analytics.

## 📊 Project Overview

This project implements a fully functional grocery store database with:
- **200+ customers** with detailed profiles
- **50+ products** across multiple categories
- **300+ orders** with complete transaction details
- **Advanced business intelligence queries** for sales analysis

## 🗃️ Database Schema

### Tables Structure
- **Customers** - Customer information and addresses
- **Products** - Product details, pricing, and categorization
- **Suppliers** - Supplier information and relationships
- **Categories** - Product categorization
- **Employees** - Staff management
- **Orders** - Order headers and dates
- **Order_Details** - Line items with quantities and pricing

### Entity-Relationship Diagram

![Grocery Store DB ER Diagram](https://github.com/VenkataSateesh8/Grocery-Store-Database-Management-System/blob/main/Images/Grocery_Store_DB_ER_Diagram.png)



## 🚀 Features

### Business Intelligence
- **Customer Analytics**: Purchase patterns and loyalty analysis
- **Product Performance**: Sales volume and revenue tracking
- **Supplier Analysis**: Contribution and performance metrics
- **Employee Performance**: Order processing efficiency
- **Sales Trends**: Monthly and seasonal analysis

### Operational Management
- Complete inventory tracking
- Order processing system
- Supplier relationship management
- Customer engagement tracking

## 📁 File Structure

```
Grocery_Store_Database/
├── README.md
├── Grocery_Management_Project.sql  # Main file (keep this)
├── database_schema.sql            # Only CREATE statements
├── sample_data.sql               # Only INSERT statements  
├── analysis_queries.sql          # Only SELECT queries
├── images/
│   └── er_diagram.png           # Visual diagram
└── results/
    └── sample_outputs.md        # Query outputs
```

## 🛠️ Installation & Setup

### Prerequisites
- MySQL Server 8.0+
- MySQL Workbench or similar SQL client

### Database Setup
1. Clone the repository:
```
git clone https://github.com/VenkataSateesh8/Grocery-Store-Database-Management-System.git
cd Grocery-Store-Database-Management-System
```

2. Execute the database creation script:
```
SOURCE database_schema.sql;
```

3. Load sample data:
```
SOURCE sample_data.sql;
```

4. Run analysis queries:
```
SOURCE analysis_queries.sql;
```

## 📈 Key Analyses Included
### Customer Insights
- Customer engagement metrics
- Top customers by purchase value
- Customer loyalty patterns

### Product Performance
- Best-selling products
- Category-wise performance
- Pricing strategy analysis

### Sales Analytics
- Monthly revenue trends
- Order pattern analysis
- Seasonal performance

### Operational Metrics
- Employee performance tracking
- Supplier contribution analysis
- Inventory turnover rates


## 📊 Sample Queries
### Customer Lifetime Value
```sql
SELECT c.customer_name, SUM(od.total_price) AS total_spent
FROM customers c 
JOIN orders o ON c.customer_id = o.customer_id
JOIN order_details od ON o.order_id = od.order_id
GROUP BY c.customer_id 
ORDER BY total_spent DESC LIMIT 5;
```

### Monthly Revenue Growth
```sql
SELECT YEAR(order_date) AS year, MONTH(order_date) AS month,
       SUM(total_price) AS monthly_revenue
FROM orders o JOIN order_details od ON o.order_id = od.order_id
GROUP BY year, month ORDER BY year, month;
```

### Introduction

The Grocery Store Management System is a database project developed to apply SQL concepts in a real-life scenario. It aims to store, manage, and organize grocery-related data such as products, suppliers, customers, employees, categories, and orders in a systematic manner.

This project demonstrates how databases help maintain accurate records and simplify daily operations in a store. By designing tables and defining relationships between them, it becomes easier to track which customer ordered which product, which supplier provides which items, and how sales are processed.

The system uses SQL features like primary keys, foreign keys, and cascading options to maintain data integrity and consistency. Queries are used to insert new records, update existing details, delete unwanted data, and retrieve information for reports and analysis.

Through this project, students can understand the practical use of database normalization, relationships, and SQL queries to build a small yet efficient management system. It helps in improving data accuracy, reduces manual record-keeping, and gives hands-on experience in handling structured data for a business-like environment.


### Problem Statement

In most small grocery stores, records of products, suppliers, customers, and sales are often maintained manually. This traditional method makes it difficult to handle large amounts of data and leads to problems such as missing information, duplicate entries, and calculation errors. As the store grows, managing daily operations like tracking stock, updating prices, and maintaining order details becomes time-consuming and inefficient.

There is also no easy way to check which products are running out of stock, which suppliers are linked to which items, or how many orders have been completed on a given date. Without a proper database, generating reports and analyzing sales trends becomes difficult.

To overcome these issues, a database-based solution is needed where all information can be stored in a structured and connected form. The Grocery Store Management System aims to solve these problems by using SQL to organize and manage the store’s data efficiently, reduce manual work, and ensure quick and accurate information retrieval.



### Key Findings and Insights

Stable Pricing:
All products have fixed unit prices. no variation across orders, showing consistent and transparent pricing.
High-Demand and Low-Movement Items :
Ghee, Paneer, Moong Dal, and Basmati Rice are the most ordered and highest revenue-generating items.
Pickles and Yogurt show the lowest average quantities and revenue indicating occasional purchases.
Customer Concentration:
A small number of repeat customers contribute most of the total sales, highlighting loyalty-driven revenue.
Employee Performance Variation:
Certain employees handle significantly more orders, indicating high efficiency or workload imbalance.
Seasonal & Weekly Trends:
Order volumes peak on specific dates or months, suggesting customer shopping patterns (likely weekends or festivals).

### Conclusion

The Grocery Store Management System successfully demonstrates the practical application of SQL in managing and organizing real-world retail data. It integrates information about products, suppliers, customers, employees, and orders into a well-structured database, ensuring accuracy, consistency, and efficient data handling.
Through the implementation of primary and foreign keys, cascading relationships, and optimized queries, the system maintains data integrity and simplifies operations such as order tracking, product management, and report generation. Overall, this project highlights how a well-designed database can automate daily tasks, reduce manual errors, and provide meaningful insights making business operations more efficient, reliable, and data driven.

### Final Thought

A well-designed database is the foundation of efficient business management turning data into meaningful insights that drive smarter, faster, and more sustainable growth.




