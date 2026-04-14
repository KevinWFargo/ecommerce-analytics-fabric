# E-commerce Analytics Pipeline (Microsoft Fabric)

## Overview
This project simulates a real-world data engineering workflow using a medallion architecture (Bronze, Silver, Gold) to prepare data for analytics and reporting.

The goal is to transform raw e-commerce data into a structured data model that supports business insights such as revenue trends, customer behavior, and product performance.

---

## Architecture
This project follows a medallion architecture:

- **Bronze**: Raw data ingestion (CSV files stored in Lakehouse)
- **Silver**: Data cleaning and transformation
- **Gold**: Star schema for analytics and reporting

---

## Tech Stack
- Microsoft Fabric (Lakehouse)
- PySpark (data transformations)
- Power BI (planned for reporting)

---

## Data Pipeline Layers

- [Bronze Layer – Raw Data Ingestion](docs/bronze.md)
- [Silver Layer – Data Transformation](docs/silver.md)
- [Gold Layer – Analytical Model](docs/gold.md)

---

## Current Status
✅ Bronze layer complete  
✅ Silver layer complete  
✅ Gold layer complete  
🚧 Power BI modeling in progress  

---

## Dataset
Olist Brazilian E-commerce Dataset (public dataset)
