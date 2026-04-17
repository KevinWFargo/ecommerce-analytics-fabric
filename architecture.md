\# Architecture Overview



\## Overview



This project implements an end-to-end data pipeline using Microsoft Fabric and Power BI.



A medallion architecture (Bronze, Silver, Gold) is used to structure data as it progresses from raw ingestion to analytical modeling and visualization.



\---



\## Data Architecture



!\[Pipeline](images/fabric/pipeline.png)



The pipeline follows a layered approach:



\- \*\*Bronze Layer\*\* → Raw data ingestion from source files

\- \*\*Silver Layer\*\* → Data cleaning, validation, and transformation

\- \*\*Gold Layer\*\* → Analytical model structured as a star schema



\---



\## Data Flow



1\. Raw CSV files are ingested into the Bronze layer within the Fabric Lakehouse

2\. Data is transformed and enriched in the Silver layer using PySpark notebooks

3\. Cleaned datasets are modeled into fact and dimension tables in the Gold layer

4\. Power BI connects to the Gold layer for reporting and visualization



\---



\## Layer Responsibilities



\### Bronze Layer

\- Stores raw source data with no transformations

\- Preserves data fidelity for traceability



\### Silver Layer

\- Applies data cleaning and transformation logic

\- Filters to valid ("delivered") transactions

\- Enriches data through joins and standardization



\### Gold Layer

\- Implements a star schema for analytical queries

\- Separates fact and dimension tables

\- Optimized for performance in Power BI



\---



\## Data Model



The Gold layer is structured as a star schema:



\- \*\*Fact Table\*\*

&#x20; - `gold\_fact\_sales` (order item-level granularity)



\- \*\*Dimension Tables\*\*

&#x20; - `gold\_dim\_customers`

&#x20; - `gold\_dim\_products`

&#x20; - `gold\_dim\_sellers`

&#x20; - `gold\_dim\_date`



This model supports efficient filtering, aggregation, and time-based analysis.



\---



\## Power BI Layer



Power BI is used as the analytical and visualization layer:



\- Connects directly to Gold layer tables

\- Implements a semantic model with relationships and measures

\- Provides interactive dashboards with:

&#x20; - Drill-through functionality

&#x20; - Custom tooltips

&#x20; - Time-series analysis



\---

