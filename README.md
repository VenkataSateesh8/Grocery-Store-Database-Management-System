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






