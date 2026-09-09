# 🏗️ SQL Data Warehouse & Analytics Project

An end-to-end data warehousing and analytics solution built on **SQL Server**, taking raw CRM and ERP data through a **Medallion Architecture** (Bronze → Silver → Gold) into a business-ready star schema for reporting and analysis.

This is a portfolio project demonstrating practical data engineering skills: ETL pipeline design, data cleansing, dimensional modeling, and SQL-based analytics.

---

## 🏛️ Data Architecture

The warehouse follows the **Medallion Architecture**, with each layer serving a distinct purpose:

| Layer | Purpose | Description |
|-------|---------|-------------|
| 🥉 **Bronze** | Raw ingestion | Data loaded as-is from source CSV files (CRM & ERP) into SQL Server, with no transformations, for full traceability. |
| 🥈 **Silver** | Cleansing & standardization | Data is cleaned, deduplicated, standardized, and normalized to prepare it for analysis. |
| 🥇 **Gold** | Business-ready | Data modeled into a **star schema** (fact & dimension tables/views) optimized for reporting and analytics. |

```
CSV Sources (CRM + ERP)
        │
        ▼
   🥉 Bronze Layer   (raw, untouched)
        │
        ▼
   🥈 Silver Layer   (cleaned, standardized)
        │
        ▼
   🥇 Gold Layer     (star schema, business-ready)
        │
        ▼
   BI / Reporting / SQL Analytics
```

---

## 📖 Project Overview

This project covers the full data warehousing lifecycle:

- **Data Architecture** — Designing a modern warehouse using the Bronze/Silver/Gold layering pattern.
- **ETL Pipelines** — Extracting, transforming, and loading data from CRM and ERP source systems.
- **Data Modeling** — Building fact and dimension tables optimized for analytical queries (star schema).
- **Analytics & Reporting** — Writing SQL queries to surface insights on customer behavior, product performance, and sales trends.

### Objective

Consolidate CRM and ERP sales data from two source systems into a single, well-modeled SQL Server data warehouse that supports reliable analytical reporting.

### Specifications

- **Data Sources**: CSV exports from two systems — CRM and ERP.
- **Data Quality**: Source data is cleansed and quality issues are resolved before modeling.
- **Integration**: Both sources are merged into one unified, analytics-friendly data model.
- **Scope**: Latest snapshot only — historical tracking (SCD) is out of scope.
- **Documentation**: Data model and ETL logic are documented for both engineers and business users.

---

## 🛠️ Tools & Technologies

- **Microsoft SQL Server** (Express) — database engine
- **SQL Server Management Studio (SSMS)** — database management GUI
- **T-SQL** — ETL scripts, stored procedures, and views
- **Draw.io** — architecture, data flow, and data model diagrams
- **Git & GitHub** — version control

---

## 📂 Repository Structure

```
sql-data-warehouse-project/
│
├── datasets/                  # Raw source data (CRM & ERP CSV files)
│
├── docs/                      # Documentation & diagrams
│   ├── data_architecture.drawio   # Overall warehouse architecture
│   ├── data_flow.drawio           # Data flow diagram
│   ├── data_models.drawio         # Star schema / data models
│   ├── etl.drawio                 # ETL techniques and methods
│   ├── data_catalog.md            # Field-level dataset catalog
│   └── naming-conventions.md      # Naming conventions for tables/columns/files
│
├── scripts/                   # SQL scripts for ETL and transformations
│   ├── bronze/                 # Raw data ingestion scripts
│   ├── silver/                 # Cleansing & transformation scripts
│   └── gold/                   # Star schema / analytical view scripts
│
├── tests/                     # Data quality and validation scripts
│
├── README.md                  # Project overview (this file)
├── LICENSE                    # MIT license
└── requirements.txt           # Project dependencies
```

---

## 🚀 Getting Started

1. **Set up SQL Server**: Install SQL Server Express and SSMS.
2. **Clone the repo**:
   ```bash
   git clone https://github.com/AtharvaVSawant/sql-data-warehouse-project.git
   ```
3. **Run the Bronze scripts** (`scripts/bronze/`) to create schemas and load raw CSVs from `datasets/`.
4. **Run the Silver scripts** (`scripts/silver/`) to clean and standardize the data.
5. **Run the Gold scripts** (`scripts/gold/`) to build the star schema views.
6. **Explore**: Query the Gold layer views directly in SSMS, or connect a BI tool (Power BI, Tableau) for dashboards.

For detailed requirements, see [`docs/requirements.md`](docs/requirements.md). For the data catalog, see [`docs/data_catalog.md`](docs/data_catalog.md).

---

## 📊 Analytics & Insights

SQL-based analysis built on top of the Gold layer covers:

- **Customer Behavior** — segmentation, purchase patterns
- **Product Performance** — top/bottom performers, category trends
- **Sales Trends** — time-series and cumulative sales analysis

---

## 🛡️ License

This project is licensed under the [MIT License](LICENSE) — free to use, modify, and share with attribution.

---

## 👤 About

Built by **Atharva Sawant** as a portfolio project to demonstrate data engineering and analytics skills using SQL Server.

- GitHub: [AtharvaVSawant](https://github.com/AtharvaVSawant)
- LinkedIn: [atharvavsawant](https://linkedin.com/in/atharvavsawant)
