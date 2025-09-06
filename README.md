# Zepto-SQL-Project

This project is a **SQL-based analysis of Zepto's product dataset**, showcasing database design, data exploration, and query execution.  
It demonstrates how to create tables, insert data, and perform SQL operations to analyze discounts, availability, and pricing patterns.

---

## 📑 Table of Contents

- [Project Overview](#project-overview)
- [Files](#files)
- [Database Schema](#database-schema)
- [Requirements](#requirements)
- [Setup](#setup)
- [Usage](#usage)
- [Sample Queries](#sample-queries)
- [Contributing](#contributing)
- [License](#license)

---

## 📌 Project Overview

Zepto is a quick-commerce platform that delivers groceries and essentials.  
This project simulates a **Zepto product database** to analyze:

- Product categories and availability  
- Discounts and pricing trends  
- Stock management (out-of-stock vs in-stock items)  
- Exploratory queries on real-world-like datasets  

---

## 📂 Files

- **`zepto_SQL_project.sql`** → Contains SQL scripts to:
  - Create the `zepto` table  
  - Insert and explore data  
  - Run queries for insights  

- **`zepto_v2.csv`** → Dataset with product information such as:
  - `sku_id`, `category`, `name`  
  - `mrp`, `discountPercent`, `discountedSellingPrice`  
  - `availableQuantity`, `weightInGms`, `outOfStock`  

---

## 🗄️ Database Schema

The project creates a single table `zepto`:

| Column Name              | Data Type        | Description |
|---------------------------|-----------------|-------------|
| `sku_id`                 | SERIAL (PK)     | Unique product ID |
| `category`               | VARCHAR(120)    | Product category |
| `name`                   | VARCHAR(150)    | Product name |
| `mrp`                    | NUMERIC(8,2)    | Maximum Retail Price |
| `discountPercent`        | NUMERIC(5,2)    | Discount offered (%) |
| `availableQuantity`      | INTEGER         | Quantity available |
| `discountedSellingPrice` | NUMERIC(8,2)    | Final price after discount |
| `weightInGms`            | INTEGER         | Weight of product (grams) |
| `outOfStock`             | BOOLEAN         | Availability flag |
| `quantity`               | INTEGER         | Ordered quantity |

---

## ⚙️ Requirements

- PostgreSQL (preferred) or any SQL-compatible RDBMS  
- SQL client (e.g., pgAdmin, DBeaver, or psql CLI)  
- Python (optional, if analyzing CSV with Pandas)  

---

## 🚀 Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/prakrutiparmar/Zepto-SQL-Project.git
   cd Zepto-SQL-Project
   ````

 2. Open PostgreSQL and run the SQL script:
 ```bash
 \i zepto_SQL_project.sql
````
3. Import the CSV for additional analysis:
 ```bash
COPY zepto(category, name, mrp, discountPercent, availableQuantity, discountedSellingPrice, weightInGms, outOfStock, quantity)
FROM 'path/to/zepto_v2.csv'
DELIMITER ','
CSV HEADER; 
````

## 📊 Usage

Once the database is set up, you can:
- Explore product data 
- Calculate discounts and margins 
- Identify stock availability
- Run business-oriented queries

## 🤝 Contributions 
Contributions are welcome! Feel free to fork this repo, make improvements, and open a pull request.
