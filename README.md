# 📦 Shipping Management System – PL/SQL Capstone Project

This project is part of the AUCA PL/SQL Capstone Examination. It presents a fully functional database system for managing shipping operations, built in Oracle SQL using PL/SQL features. The system tracks customer orders, packages, delivery personnel, warehouse operations, payments, and feedback.

---

## 📌 Project Objective

To develop a Shipping Management System that enhances order processing, reduces manual errors, and improves visibility across the entire logistics chain. The system is designed to support real-world operations such as order placement, warehouse dispatching, package tracking, payment processing, and customer feedback.

---

## ✅ Project Phases

### Phase I: Problem Statement
Describes the challenges in logistics management and proposes an Oracle database solution for efficient shipping operations.

### Phase II: Business Process Modeling
Provides a BPMN diagram and flow explanation for the complete order-to-delivery lifecycle, showing interaction between system actors (customers, warehouse staff, logistics managers, and delivery personnel).

### Phase III: Logical Model Design
Defines the data model with an Entity-Relationship Diagram (ERD), identifying entities, attributes, relationships, and normalization up to 3NF.

### Phase IV: Physical Model Design
Translates the logical model into SQL `CREATE TABLE` statements with constraints (PKs, FKs, NOT NULL, UNIQUE, CHECK).

### Phase V: Table Implementation & Data Insertion
Implements the full schema and inserts sample data for testing, using `INSERT INTO` statements. Tables include:

- `Customer`
- `Warehouse`
- `ShippingOrder`
- `Package`
- `DeliveryPersonnel`
- `Payment`
- `Feedback`

### Phase VI: SQL Queries and Insights
Demonstrates useful queries for business decision-making, including joins, filters, aggregation (`COUNT`, `AVG`), and status tracking.

### Phase VII: Final Presentation
Summarizes the entire project through slides, diagrams, and sample outputs. Screenshots of tables and queries are included for demonstration.

---

## 🗂️ Project Files

| File/Folder           | Description                              |
|-----------------------|------------------------------------------|
| `create_tables.sql`   | SQL script to create all project tables  |
| `insert_data.sql`     | SQL script to insert sample data         |
| `queries.sql`         | SQL queries for Phase VI                 |
| `ERD.png`             | Logical Entity-Relationship Diagram      |
| `BPMN.png`            | Business Process Model (Order lifecycle) |
| `README.md`           | Project overview and documentation       |
| `FinalPresentation.pptx` | Summary slides for project phases      |

---

## 👤 Developer Info

- **Name**: [Your Full Name]
- **Course**: PL/SQL Capstone – AUCA
- **Submission Date**: [Month Year]

---

## 🚀 How to Run

1. Copy the SQL scripts into [https://livesql.oracle.com](https://livesql.oracle.com) or use Oracle SQL Developer Web.
2. Run `create_tables.sql` to set up the schema.
3. Run `insert_data.sql` to populate tables with test data.
4. Use `queries.sql` to explore data and extract insights.

---

## 📈 Sample Query Output

```sql
-- List all orders with customer and warehouse info
SELECT 
  so.OrderID,
  c.FullName AS Customer,
  w.Location AS Warehouse,
  so.OrderStatus
FROM ShippingOrder so
JOIN Customer c ON so.CustomerID = c.CustomerID
JOIN Warehouse w ON so.WarehouseID = w.WarehouseID;
