# 🏗️ ETL & DDL SQL Scripts — Data Warehouse Pipeline

This repository module defines the **core ETL (Extract, Transform, Load)** structure and **DDL (Data Definition Language)** scripts used to create and populate the **Bronze, Silver, and Gold layers** of the Data Warehouse.  
These scripts are the foundation for maintaining structured, validated, and analytics-ready datasets.

---

## 📁 Repository Structure
sql_scripts/
├── ddl_bronze.sql
├── proc_load_bronze.sql
├── ddl_silver.sql
├── proc_load_silver.sql
└── ddl_gold.sql
---

## ⚙️ Overview of Layers

| Layer | Description | Purpose |
|-------|--------------|----------|
| **Bronze** | Raw ingestion layer | Captures unprocessed CRM & ERP data directly from source systems. |
| **Silver** | Cleansed transformation layer | Cleans, validates, and standardizes raw data for analytical use. |
| **Gold** | Curated analytics layer | Stores final fact and dimension tables ready for BI dashboards and reports. |

---

| No. | File | Description | Download |
|----:|------|--------------|-----------|
| 1 | ddl_bronze.sql | Creates Bronze layer schema (raw tables). | [Get this file](./ddl_bronze.sql) |
| 2 | proc_load_bronze.sql | Loads raw CRM & ERP data into Bronze tables. | [Get this file](./proc_load_bronze.sql) |
| 3 | ddl_silver.sql | Defines Silver layer schema (cleaned, standardized tables). | [Get this file](./ddl_silver.sql) |
| 4 | proc_load_silver.sql | Transforms and loads Bronze → Silver. | [Get this file](./proc_load_silver.sql) |
| 5 | ddl_gold.sql | Creates Gold layer schema (fact and dimension tables). | [Get this file](./ddl_gold.sql) |
---

## 🔄 ETL Flow Summary

1. **Bronze Layer (Raw)**  
   - Data is extracted from CRM and ERP systems.  
   - Stored using `ddl_bronze.sql`.  
   - Loaded via `proc_load_bronze.sql`.

2. **Silver Layer (Cleansed)**  
   - Standardization, data cleaning, and transformation occur.  
   - Schema created by `ddl_silver.sql`.  
   - Data loaded via `proc_load_silver.sql`.

3. **Gold Layer (Analytics)**  
   - Final dimensional modeling (Facts & Dimensions).  
   - Schema built using `ddl_gold.sql`.  
   - Consumed by Power BI / Tableau dashboards.

---

## 🧠 Objective

To build a modular, maintainable ETL framework ensuring:
- Clean separation between raw, processed, and analytical data.  
- Consistent schema design across all layers.  
- Easy automation via stored procedures.  
- High scalability for large CRM/ERP datasets.

---

## 💡 Best Practices Implemented
- Naming conventions for schemas and tables (BRZ_, SLV_, GLD_ prefixes).  
- Timestamp tracking for incremental loads.  
- Error handling and data validation at each stage.  
- Modular script design for easy maintenance.  

---

## 👨‍💻 Author


**Ravi Nandan Yadav**  
📍 Gaya, India  
📧 [ravinandanyadavwork@gmail.com](mailto:ravinandanyadavwork@gmail.com)  
🔗 [GitHub Repository](https://github.com/ravi-nandan-yadav/sql-data-analytics-project)
LinkedIN: https://www.linkedin.com/in/ravi-nandan-yadav-156a6a15a/
Contact Number: 8507528999/8210710109

---

## ⭐ How to Run

1. Execute `ddl_bronze.sql` to initialize the raw data schema.  
2. Run `proc_load_bronze.sql` to populate Bronze tables.  
3. Execute `ddl_silver.sql` and `proc_load_silver.sql` sequentially.  
4. Finally, run `ddl_gold.sql` to prepare the analytical layer.  

Each step can be automated through scheduling or orchestration tools (e.g., Airflow, SSIS, or Azure Data Factory).

---
