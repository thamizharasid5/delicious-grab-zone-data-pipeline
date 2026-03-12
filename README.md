🥐 Delicious Grab Zone Data Pipeline


📖 Overview

This project demonstrates an end‑to‑end ETL pipeline built on Azure Databricks, Delta Lake, and PySpark, using authentic bakery business data.
It showcases data engineering best practices: cleaning, transformations, aggregations, Delta Lake storage, and automated scheduling with Databricks Jobs.



✨ Features


✅ Delta Lake storage for reliability and performance

✅ PySpark transformations for scalable data processing

✅ Data quality checks with deduplication, null handling, and schema validation

✅ Databricks Jobs automation (manual run + scheduled trigger)

✅ Parameterization using job parameters (target_table, start_date, end_date)

✅ GitHub integration for version control and portfolio presentation

✅ Unity Catalog migration for governance and performance




🛠️ Technologies Used


Azure Databricks → ETL orchestration and PySpark transformations

Delta Lake (Bronze → Silver → Gold zones) → Curated storage layers

Azure Data Factory (ADF) → Scheduling and triggers

PySpark / SQL → Transformations and aggregations

GitHub → Version control and CI/CD integration



📊 Dataset

Authentic Bakery Sales Data with fields:

Sale ID, Product, Quantity, Amount, Sale Date, Customer ID

Used to demonstrate daily revenue trends, top‑selling products, and premium customers




🏗️ Architecture

mermaid
graph TD
    A[Raw Bakery Sales - Bronze] --> B[Cleaning & Deduplication - Silver]
    B --> C[Transformations & Aggregations - Gold]
    C --> D[Curated Delta Tables for Analytics]



📐 Project Structure

Code
delicious-grab-zone-etl-pipeline/
├── notebooks/
│   ├── 01_delicious_grab_zone_clean.ipynb
│   ├── 02_delicious_grab_zone_transformations.ipynb
│   ├── 03_delicious_grab_zone_aggregations.ipynb
│   └── 04_delicious_grab_zone_delta_pipeline.ipynb
├── configs/
│   └── parameters.json
├── README.md
├── .gitignore
└── LICENSE



⚙️ Notebook Flow

01_clean → Load raw bakery data, clean missing values, standardize formats

02_transformations → Apply business rules, enrich data, create transformed Delta tables

03_aggregations → Generate insights (monthly revenue, top customers, top items) with PySpark aggregations and window functions

04_delta_pipeline → Final orchestration notebook: saves curated tables, registers them in Databricks SQL, and is scheduled as a Databricks Job



🚀 How to Run


Import notebooks into Databricks

Run them in sequence: 01 → 02 → 03 → 04

Create a Databricks Job for 04_delicious_grab_zone_delta_pipeline.ipynb

Configure cluster, parameters, and trigger (e.g., daily at 2 AM IST)

Verify Delta tables in Databricks SQL with queries



📊 Monitoring

Databricks Job Runs → Track task durations and statuses

Spark UI → Identify shuffle bottlenecks, skew, and disk spills

Delta Tables → Query curated outputs for insights



🎯 Business Impact


Automated daily bakery sales reporting

Identified premium customers and revenue trends for better decision‑making

Enabled management to plan inventory and promotions effectively



📜 License

This project is licensed under the MIT License — see the LICENSE file for details
