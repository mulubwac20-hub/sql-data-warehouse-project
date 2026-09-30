# sql-data-warehouse-project
# Data Warehouse and Analytics Project 

A comprehensive data warehousing and analytics solution, from building a data warehouse in SQL Server to generating actionable business insights.

> ## 🙏 Credit
> This project was **created by Baraa Khatib Salkini ([Data With Baraa](https://www.youtube.com/@DataWithBaraa))**. All credit for the original concept, architecture, dataset, documentation, and project design goes to him. This repository is my own walkthrough / implementation of his project, built for learning and portfolio purposes. If you want the original material, tutorials, and project templates, please go to his channels.

---

## 🏗️ Data Architecture

The project follows the **Medallion Architecture** with **Bronze**, **Silver**, and **Gold** layers.

| Layer | Purpose |
|-------|---------|
| 🥉 **Bronze** | Stores raw data as-is from the source systems. Data is ingested from CSV files into a SQL Server database. |
| 🥈 **Silver** | Data cleansing, standardization, and normalization to prepare data for analysis. |
| 🥇 **Gold** | Business-ready data modeled into a **star schema** for reporting and analytics. |

```
CSV Files (ERP + CRM)  ──▶  Bronze (raw)  ──▶  Silver (clean)  ──▶  Gold (star schema)  ──▶  Analytics & Reporting
```

---

## 📖 Project Overview

This project covers:

1. **Data Architecture** – Designing a modern data warehouse using the Medallion Architecture.
2. **ETL Pipelines** – Extracting, transforming, and loading data from source systems into the warehouse.
3. **Data Modeling** – Developing fact and dimension tables optimized for analytical queries.
4. **Analytics & Reporting** – Creating SQL-based reports and dashboards for actionable insights.

🎯 It's a useful resource for anyone looking to build skills in:

- SQL Development
- Data Architecture
- Data Engineering
- ETL Pipeline Development
- Data Modeling
- Data Analytics

---

## 🔄 ETL Methods Reference


### Extraction
- **Extraction methods:** Pull extraction
- **Extract types:** Full extraction
- **Extract techniques:** File parsing

### Transformation
- **Data cleansing:** Remove duplicates, Data filtering, Handling missing data, Handling invalid values, Handling unwanted spaces, Data type casting, Outlier detection
- **Data enrichment**
- **Data integration**
- **Derived columns**
- **Data normalization & standardization**
- **Business rules & logic**
- **Data aggregations**

### Load
- **Processing types:** Batch processing
- **Load methods:**
  - *Full load:* Truncate & insert, Upsert, Drop-create-insert
    
-**Slowly Changing Dimensions (SCD)**:  SCD 1 (overwrite) 

> In this project, the scope is the **latest dataset only**, so historization (SCD 2) is not required.

---

## 🚀 Project Requirements

### Building the Data Warehouse (Data Engineering)

**Objective:** Develop a modern data warehouse using SQL Server to consolidate sales data, enabling analytical reporting and informed decision-making.

**Specifications**
- **Data Sources:** Import data from two source systems (ERP and CRM) provided as CSV files.
- **Data Quality:** Cleanse and resolve data quality issues prior to analysis.
- **Integration:** Combine both sources into a single, user-friendly data model designed for analytical queries.
- **Scope:** Focus on the latest dataset only; historization of data is not required.
- **Documentation:** Provide clear documentation of the data model to support both business stakeholders and analytics teams.

### BI: Analytics & Reporting (Data Analysis)

**Objective:** Develop SQL-based analytics to deliver detailed insights into:

- **Customer Behavior**
- **Product Performance**
- **Sales Trends**

These insights give stakeholders key business metrics to support strategic decision-making.

---

## 🛠️ Tools & Resources

Everything used in this project is free:

- **Datasets:** The project dataset (CSV files for ERP and CRM)
- **[SQL Server Express](https://www.microsoft.com/en-us/sql-server/sql-server-downloads):** Lightweight server for hosting the SQL database
- **[SQL Server Management Studio (SSMS)](https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms):** GUI for managing and interacting with databases
- **[Git & GitHub](https://github.com):** Version control and collaboration
- **[Draw.io](https://www.drawio.com/):** Designing data architecture, models, flows, and diagrams
- **Notion:** Project template and step-by-step project phases (available via the original creator's channels)

---

## 📂 Repository Structure

```
data-warehouse-project/
│
├── datasets/                           # Raw datasets used for the project (ERP and CRM data)
│
├── docs/                               # Project documentation and architecture details
│   ├── etl.drawio                      # Draw.io file showing the different techniques and methods of ETL
│   ├── data_architecture.drawio        # Draw.io file showing the project's architecture
│   ├── data_catalog.md                 # Catalog of datasets, including field descriptions and metadata
│   ├── data_flow.drawio                # Draw.io file for the data flow diagram
│   ├── data_models.drawio              # Draw.io file for data models (star schema)
│   ├── naming-conventions.md           # Consistent naming guidelines for tables, columns, and files
│
├── scripts/                            # SQL scripts for ETL and transformations
│   ├── bronze/                         # Scripts for extracting and loading raw data
│   ├── silver/                         # Scripts for cleaning and transforming data
│   ├── gold/                           # Scripts for creating analytical models
│
├── tests/                              # Test scripts and quality checks
│
├── README.md                           # Project overview and instructions
├── LICENSE                             # License information for the repository
├── .gitignore                          # Files and directories to be ignored by Git
└── requirements.txt                    # Dependencies and requirements for the project
```

---

## ▶️ Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/data-warehouse-project.git
   ```
2. **Install** SQL Server Express and SSMS.
3. **Create the database and schemas** (`bronze`, `silver`, `gold`).
4. **Bronze:** Run the scripts in `scripts/bronze/` to load the raw CSV files.
5. **Silver:** Run the scripts in `scripts/silver/` to clean and standardize the data.
6. **Gold:** Run the scripts in `scripts/gold/` to build the star-schema views/tables.
7. **Analyze:** Run the SQL analytics queries to explore customer behavior, product performance, and sales trends.

---

## 🙌 Acknowledgements

Huge thanks to **Baraa Khatib Salkini (Data With Baraa)** for creating this project and sharing it freely with the community. Please support his work:

- 📺 YouTube: [Data With Baraa](https://www.youtube.com/@DataWithBaraa)
- 🌐 Website / LinkedIn: see his channel for the latest links

---

## 🛡️ License

This repository is licensed under the [MIT License](LICENSE). Note that the original project concept, dataset, and diagrams belong to their creator, Data With Baraa; please check and respect his terms for reuse of those materials.

---

## 🌟 About Me

Hi, I'm  Chama Mulubwa. I built this repository while following Baraa's data warehouse project to practice SQL, ETL, and data modeling.

- LinkedIn: https://www.linkedin.com/in/chama-mulubwa-7a9590341?utm_source=share_via&utm_content=profile&utm_medium=member_android
- GitHub: https://github.com/mulubwac20-hub
