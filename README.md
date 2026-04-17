\# E-commerce Analytics Pipeline (Microsoft Fabric)



\## 📊 Dashboard Overview



\### Sales Overview

!\[Overview](images/power\_bi/overview.png)



\### Sales Trends \& Insights

!\[Trends](images/power\_bi/trends.png)



\### Product Drill-Through

!\[Product Details](images/power\_bi/product\_details.png)



\---



\## 🔗 Live Dashboard



\[View Interactive Power BI Report](https://app.fabric.microsoft.com/view?r=eyJrIjoiOWM4MWExZDYtYjkzYi00NjM1LWExOGMtYWFlNGVmN2RmZjkzIiwidCI6IjNhNDA4NTc1LTdiNWMtNGRhOC1hNzRkLTNhNGQ3MDA4NjU0ZCJ9\&pageName=0ecc507036c284b78dd3)



\---



\## 🧠 Project Overview



This project simulates an end-to-end data engineering and analytics workflow using Microsoft Fabric and Power BI.



A medallion architecture (Bronze, Silver, Gold) is implemented to transform raw e-commerce data into a clean, structured model that powers an interactive dashboard.



The solution enables analysis of:

\- Revenue trends over time

\- Product and category performance

\- Order volume and customer behavior



\---



\## 🧩 End-to-End Solution



This project demonstrates both data engineering and analytics capabilities:



\- \*\*Microsoft Fabric\*\* → Data ingestion, transformation, and modeling (Bronze → Silver → Gold)

\- \*\*Power BI\*\* → Semantic modeling, DAX measures, and interactive dashboards



\---



\## 🏗️ Architecture



!\[Pipeline](images/fabric/pipeline.png)



This project follows a medallion architecture:



\- \*\*Bronze\*\* → Raw ingestion of source data (CSV files stored in Lakehouse)

\- \*\*Silver\*\* → Cleaned, filtered, and enriched datasets

\- \*\*Gold\*\* → Star schema optimized for analytical queries and reporting



\---



\## ⚙️ Tech Stack



\- Microsoft Fabric (Lakehouse)

\- PySpark (data transformations)

\- Power BI (data modeling \& visualization)



\---



\## 📦 Data Pipeline Layers



\- \[Bronze Layer – Raw Data Ingestion](docs/bronze.md)

\- \[Silver Layer – Data Transformation](docs/silver.md)

\- \[Gold Layer – Analytical Model](docs/gold.md)



\---



\## 📈 Key Insights



\- Revenue shows a steady upward trend with noticeable spikes during peak periods

\- A small number of product categories drive the majority of total revenue

\- Order volume and revenue are strongly correlated

\- Product-level drill-through enables granular performance analysis



\---



\## 📊 Data Model



!\[Data Model](images/power\_bi/data\_model.png)



The Gold layer is structured as a star schema:

\- `gold\_fact\_sales` (fact table)

\- Dimension tables for customers, products, sellers, and date



\---



\## 📂 Dataset



\[Olist Brazilian E-commerce Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

