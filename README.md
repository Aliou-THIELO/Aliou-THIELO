# Aliou THIELO — Data Engineer & MLOps 🇸🇳

<p>🎓 M1 Statistical Modeling & Computer Science, Data Science Track — Double Degree UCAD Dakar · Université de Lille, France</p>
<p>📚 Data Engineering Training — Force-N Program (in progress)</p>
<p>📍 Dakar, Senegal</p>
---

## 👋 About Me

I'm a Data Engineer in training based in Dakar, Sénégal, building reliable, scalable, production-grade data pipelines — from API ingestion to cloud deployment on AWS, with a business-facing visualization layer for decision-makers.

My flagship project focuses on fintech (exchange rate data for the WAEMU zone), but the underlying skills — ingestion, transformation, orchestration, ML, cloud — are domain-agnostic and directly transferable to other data-driven sectors (health, agriculture, public data, and beyond).

> This portfolio is a self-driven initiative, built progressively alongside my M1/M2 studies to gain the practical skills the job market expects — not coursework. Status per project is tracked honestly below.

---

## 🎯 Flagship Project — FCFA Exchange Rate Decision Pipeline

### The Problem

Across Senegal and the WAEMU zone, economic actors (importing merchants, SMEs, families receiving remittances) face daily fluctuations of the FCFA against major currencies (USD, EUR, CNY). The lack of centralized historical data and accessible analysis tools prevents them from spotting trends and choosing the right moment for their currency exchange operations — decisions are often made blindly.

### The Solution

An automated pipeline that collects, validates, historizes, and surfaces daily exchange rate data (XOF/USD, XOF/EUR, XOF/CNY), making these trends visible and actionable — from raw API ingestion to a business-facing dashboard.

### The Impact

Once historical data is collected and explored, the goal is to quantify the concrete gain available to users — for example, the average spread between the worst and best day of the month to exchange a given amount. This will be measured against real data, not assumed upfront.

### Why USD, EUR & CNY

The FCFA is pegged to the euro at a fixed parity guaranteed by the French Treasury, so XOF/EUR is structurally low-volatility — it mainly serves as a stable reference point. The real dynamic to track is XOF/USD, since the FCFA fluctuates indirectly against the dollar via the EUR/USD rate. Senegal also has growing trade ties with China, particularly for imports — merchants often settle with suppliers in USD or CNY. The pipeline covers XOF/CNY as well, directly addressing this user segment.

---

## 🚀 Main Pipeline — Data Engineering & MLOps

**One connected pipeline, from raw data to cloud production.**

| # | Project | Stack | Status |
|---|---|---|---|
| P1 | [📥 FCFA Exchange Rate Ingestion](https://github.com/Aliou-THIELO/p1-fcfa-exchange-rate) | Python · REST API · Pydantic · Parquet | 🔄 In progress |
| P2 | 🔄 Data Transformation Layer | dbt · DuckDB · PostgreSQL · 3-layer architecture | ⏳ Planned |
| — | 🔍 Exploratory Data Analysis | Streamlit | ⏳ Planned |
| P3 | ⚙️ Pipeline Orchestration | Apache Airflow · Docker | ⏳ Planned |
| — | 📊 Business Dashboard | Power BI (fed by the orchestrated, automated pipeline) | ⏳ Planned |
| P4 | 🤖 ML Credit Scoring Model | Scikit-learn · MLflow | ⏳ Planned |
| P5 | 🚀 Model Deployment API | FastAPI · Docker | ⏳ Planned |
| P6 | ☁️ End-to-End Cloud Pipeline | AWS S3 · Glue · Athena · Redshift | ⏳ Planned |

**The logic:** P1 feeds P2 → transformed data is explored via Streamlit (EDA: means, volatility, trends) for manual validation → P3 automates P1+P2, so the pipeline runs on a schedule rather than manual triggers → once automated, it feeds the Power BI business dashboard, reflecting a live pipeline rather than a manual snapshot → P4 (ML) is trained on P2 data → P5 deploys P4 → P6 migrates the full pipeline to AWS, in preparation for the AWS Certified Data Engineer – Associate certification.

---

## 🧱 Big Data at Scale — Standalone Module

**Independent technical demonstration — not part of the main data flow above.**

The pipeline above runs on real but low-volume data (one exchange rate per currency per day). To demonstrate Big Data tooling used in large financial institutions (banks, telcos) at a realistic scale, this module runs separately, on an independently generated, high-volume simulated dataset (via Mockaroo — high-frequency exchange transactions).

| Project | Stack | Status |
|---|---|---|
| Big Data Ingestion & Processing at Scale | Apache NiFi · Apache Spark (PySpark) · Mockaroo | ⏳ Planned |

This separation is deliberate: using Spark on a handful of daily rows would be technically unjustified. This module exists to show *when* and *why* these tools are used — not just that I can name them. It is scheduled after the main pipeline, once Data Engineering fundamentals (SQL, Python, the full P1–P6 flow) are solidly in place.

---

## 🛠️ Tech Stack

| Layer | Tools |
|---|---|
| Ingestion | Python · REST API · Pydantic · Parquet |
| Transformation | dbt · DuckDB · PostgreSQL · SQL |
| Exploration & Visualization | Streamlit · Power BI |
| Orchestration | Apache Airflow · Docker |
| Big Data (standalone module) | Apache NiFi · Apache Spark (PySpark) · Mockaroo |
| ML & MLOps | Scikit-learn · MLflow · FastAPI |
| Cloud | AWS S3 · Glue · Athena · Redshift |
| Versioning | Git · GitHub |

---

## 🎯 Domains of Application

**Currently: Fintech & Banking — West Africa** *(illustrated by the flagship project above)*

The flagship project targets real problems faced by financial institutions in Senegal and the WAEMU zone:

- 📊 Financial data pipelines (exchange rates, transactions)
- 🏦 Credit scoring for banking & microfinance
- ☁️ Cloud-native data infrastructure on AWS
- 🧱 Big Data tooling for high-volume, high-frequency financial data

The pipeline architecture itself is domain-agnostic — the same ingestion → transformation → orchestration → ML → cloud approach applies equally well to health, agricultural, or public-sector data.

---

## 📈 Current Focus

- ✅ P1 ingestion client complete — robust API client with retry logic, custom exception handling, and structured logging
- 🔄 Adding Pydantic validation layer to P1

## 📫 Let's Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Aliou%20THIELO-0077B5?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/aliou-thielo-815bba389)
[![Email](https://img.shields.io/badge/Email-thieloaliou25%40gmail.com-D14836?logo=gmail&logoColor=white)](mailto:thieloaliou25@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-Aliou--THIELO-181717?logo=github&logoColor=white)](https://github.com/Aliou-THIELO)
