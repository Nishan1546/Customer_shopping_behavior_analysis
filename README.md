# 📊 End-to-End Data Analytics Portfolio Project: Customer Shopping Behavior Analysis

[![Tech Stack](https://img.shields.io/badge/Stack-Python%20%7C%20SQL%20%7C%20Power%20BI-blue.svg)](#-tools--technologies)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

A corporate-grade, end-to-end data analytics project mapping the complete lifecycle of corporate data workflows. The project takes raw customer transactional datasets, applies advanced statistical imputation and clean feature engineering in Python, handles transactional analysis through a relational SQL database, and delivers stakeholder-ready business insights via an interactive Power BI dashboard and an AI-generated presentation deck.

---

## 🛠️ Tools & Technologies
* **Data Manipulation & Cleaning:** Python 3.x (`Pandas`, `Jupyter Notebook`)
* **Statistical Insights:** `TextBlob` (NLP / Sentiment Analysis tracking for feedback loops)
* **Relational Database Engine:** PostgreSQL (Compatible with MySQL / MS SQL Server via `SQLAlchemy` & `psycopg2`)
* **Business Intelligence & Visualization:** Power BI Desktop
* **Stakeholder Reporting:** AI Documentation Frameworks (`Gamma App` for minimal deck presentation)

---

## 🏗️ Project Architecture & Workflow

The workflow mirrors enterprise operations structured into 6 clear milestones:

```text
┌─────────────────┐      ┌─────────────────────┐      ┌──────────────────┐
│ 1. Data Ingest  │ ───> │ 2. Python Cleaning  │ ───> │  3. SQL Deep-Dive│
│ Raw CSV Assets  │      │ Medians/Snake-case  │      │ CTEs & Window Fns│
└─────────────────┘      └─────────────────────┘      └──────────────────┘
                                                               │
┌─────────────────┐      ┌─────────────────────┐               │
│ 6. Git/LinkedIn │ <───  │ 5. AI Presentation  │ <───  ┌──────┴───────────┐
│ Portfolio Share │      │ Executive Deck Sync │       │4. Power BI Visual│
└─────────────────┘      └─────────────────────┘       │Interactive Report│
                                                       └──────────────────┘
```
1. Exploratory Data Analysis & Cleaning (Python)
Context-Aware Imputation: Avoided beginner bias by bypassing simple column-wide median fills. Missing review rating coordinates are dynamically imputed using the specific median rating grouped within each individual product category (e.g., matching clothing items to clothing baselines).

Database Optimization Casing: Restructured data schemas by converting irregular formatting containing uppercase string gaps directly into clean snake_case mapping lines for stress-free SQL table queries.

Feature Engineering Pipeline:

Binned customer age distributions into four clear buckets (Young Adult, Adult, Middle-Aged, Senior) via quantitative quantile cutting (pd.qcut).

Mapped textual transaction fields (Weekly, Fortnightly, Monthly) into absolute numeric tracking indicators (7, 14, 30 days) to run deep correlation arithmetic.

Redundancy Analysis: Scanned logical column pairs to find identical flags (discount_applied vs. promo_code_used), safely dropping repetitive features without data loss.

2. Advanced SQL Relational Queries
The database layer answers critical cross-demographic questions through complex queries, including:

Revenue Splits: Evaluating raw financial performance parameters grouped cleanly by customer gender lines.

Subqueries for Behavior Tracking: Separating special anomalous spend profiles where shoppers utilized discounts yet still spent higher amounts than the global product average purchase volume.

Window Functions (ROW_NUMBER): Extracting the top 3 best-selling products grouped dynamically within each parent business tier while handling matching ranking scores without dropping discrete lines.

Customer Loyalty Segmentation (CTEs): Aggregating customer purchase patterns through Common Table Expressions to classify groups into clear tiers (New, Returning, and Loyal).

3. Interactive Power BI Executive Dashboard
Dynamic Measure Building: Generated distinct database measurements utilizing explicit DAX statements capturing exact customer volumes, average financial yields, and running quality rating indexes.

UI/UX Optimization: Utilized rounded card frameworks complete with dynamic visual accents and customized borders to build corporate-level application interfaces.

Complete Interactive Slicing: Loaded custom visual segment filters enabling executive users to dynamically pivot cross-sections across gender, membership statuses, product sub-tiers, and logistics types simultaneously.

📈 Key Insights Summary
Subscriber Performance Matrix: Non-subscribed accounts accounted for a larger global volume of overall business earnings, showing key opportunities to re-evaluate the membership value proposition.

Demographic Target Zones: The Young Adult demographic generated the highest overall business returns, followed directly by middle-aged customer tiers.

Logistics Value Chains: Express shipping options generated significantly higher average transaction values than standard logistics, providing a clear signal to expand rapid delivery operations.
```
📂 Repository Layout
├── data/
│   └── customer_shopping_behavior.csv    # Raw corporate data transaction inputs
├── notebooks/
│   └── data_cleaning_exploration.ipynb   # Python EDA notebook
├── sql/
│   └── advanced_business_queries.sql     # Production SQL analysis queries
├── dashboards/
│   └── customer_behavior_report.pbix     # Packaged Power BI application dashboard
└── documentation/
    ├── project_report.pdf                 # Formal procedural summary report
    └── executive_presentation.pdf        # Stakeholder-ready AI presentation deck
```
⚡ Setup & Reproduction Guide
Prerequisites
Ensure you have a local installation of Python 3.10+, PostgreSQL (or equivalent SQL engine), and Power BI Desktop.

1. Initialize Python Environment
   python -m venv venv
source venv/bin/activate  # venv\Scripts\activate on Windows
pip install pandas sqlalchemy psycopg2 textblob
2. Run Data Pipeline & SQL Ingestion
Open and execute notebooks/data_cleaning_exploration.ipynb to clean the raw data assets.

Update the create_engine string inside the notebook to point to your local database credentials:
engine = create_engine('postgresql://username:password@localhost:5432/customer_behavior')
