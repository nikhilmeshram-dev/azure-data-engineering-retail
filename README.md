# Retail ETL Data Pipeline using Azure & Delta Lake (Medallion Architecture)

## Project Overview
This project builds an end-to-end ETL pipeline for the Retail domain using modern data engineering practices.
The pipeline ingests raw data from multiple sources, transforms it into a clean, standardized format, and loads it into a data warehouse for business reporting and analytics.

## Business Problem / Objective
- **Problem**: Retail data was scattered across multiple systems (ADLS, SQL DB, APIs), making consolidated reporting difficult.
- **Objective**:
    - Automate data ingestion from multiple sources.
    - Apply robust transformations and data modeling.
    - Deliver **business-ready datasets** for BI dashboards and decision-making.

## Key Features
 🔹 **Incremental Loading** → Implemented watermark strategy to load only new/changed data.
 🔹 **Delta Lake** → Used for ACID transactions, schema enforcement, and schema evolution.
 🔹 **SCD Type 1 & Type 2** → Managed Slowly Changing Dimensions to handle historical customer & product data.
 🔹 **Star Schema** → Designed a dimensional model with Fact & Dimension tables for analytics.
 🔹 **Partitioning & Optimization** → Improved performance using partitioning, Z-ordering, and broadcast joins in PySpark.
 🔹 **Medallion Architecture (Bronze → Silver → Gold)** →
    - **Bronze**: Raw ingested data from CSV, SQL DB, and APIs.
    - **Silver**: Cleaned, deduplicated, standardized data with business rules.
    - **Gold**: Curated fact & dimension tables for BI consumption.

## Architecture overview
<img width="1742" height="886" alt="arc" src="https://github.com/user-attachments/assets/a694eb2d-505c-42f3-ac85-112c575ce606" />

## ETL Flow
1. **Extract** – Ingest raw data into Bronze layer.
2. **Transform** – Clean, deduplicate, apply business rules in Silver layer.
3. **Load** – Build fact & dimension tables in Gold layer for analytics.

## Data Model (Star Schema)

## Technologies Used
- **Azure Data Factory** → Pipeline orchestration
- **Azure Data Lake Storage** → Bronze/Silver/Gold layers
- **Azure Databricks (PySpark)** → Data transformations
- **Delta Lake** → ACID + schema evolution
- **Azure Synapse Analytics** → Data warehouse
- **Power BI** → BI dashboards

## Challenges & Solutions


## Results
- Automated **daily ETL pipeline** with **incremental loading**.
- Centralized **retail data mart** with Sales, Inventory, and Customer tables.
- Power BI dashboards with KPIs: **Revenue, Profit Margin, Inventory Turnover**.
