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
