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


![Grocery Store DB ER Diagram](https://github.com/VenkataSateesh8/Grocery-Store-Database-Management-System/blob/main/Grocery_Store_ER_Diagram.png)

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
grocery-store-db/
├── database_schema.sql # Table creation and structure
├── sample_data.sql # Sample data insertion
├── analysis_queries.sql # Business intelligence queries
├── README.md # Project documentation
└── insights/ # Analysis results and findings


## 🛠️ Installation & Setup

### Prerequisites
- MySQL Server 8.0+
- MySQL Workbench or similar SQL client

### Database Setup
1. Clone the repository:
```bash
git clone https://github.com/yourusername/grocery-store-database.git
cd grocery-store-database
```

2. Execute the database creation script:
```bash
SOURCE database_schema.sql;
```

3. Load sample data:
```bash
SOURCE sample_data.sql;
```

4. Run analysis queries:
```bash
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

## 🎯 Sample Insights
- Top Product: Basmati Rice - Highest revenue generator
- Busiest Month: December 2022 - Peak order volume
- Best Customer: [Customer Name] - Highest total purchases
- Most Active Supplier: [Supplier Name] - Maximum product contribution


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

## 🤝 Contributing
1. Fork the repository
2. Create your feature branch (git checkout -b feature/AmazingFeature)
3. Commit your changes (git commit -m 'Add some AmazingFeature')
4. Push to the branch (git push origin feature/AmazingFeature)
5. Open a Pull Request


## 📝 License
This project is licensed under the MIT License - see the LICENSE.md file for details.

## 👥 Authors
- Your Name - Initial work

## 🙏 Acknowledgments
- Sample data generated for realistic business analysis
- SQL best practices implementation
- Comprehensive business intelligence queries



