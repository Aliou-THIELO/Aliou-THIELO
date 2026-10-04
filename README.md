# Aliou THIELO — Data Engineer & MLOps 🇸🇳

<p>🎓 M2 Modélisation Statistique et Informatique, option Data Science — Double Degree UCAD Dakar · Université de Lille, France</p>
<p>🎓 Licence 3 Informatique, Systèmes d'Information — UGB</p>
<p>📚 Data Engineering Training — Force-N Program</p>
<p>💼 Intern, AI & Data Engineering — Xarala Talent Camp, Summer 2026 (completed)</p>
<p>📍 Dakar, Senegal</p>

---

## 👋 About Me

I'm a Data Engineer in training based in Dakar, Senegal, building reliable data pipelines — from API and web ingestion to validation, storage and a business-facing visualization layer for decision-makers.

My focus is Data Engineering and MLOps for data-driven organisations in West Africa and beyond — fintech and banking, agriculture, health, public sector. I am currently learning transformation (dbt), orchestration (Airflow) and cloud (AWS), with the AWS Certified Data Engineer – Associate as my next certification goal.

The underlying skills I already apply — ingestion, validation, automated collection, testing — are domain-agnostic. I have used them on financial data (FCFA exchange rates), agricultural data, and labour-market data.

> This portfolio is a self-driven initiative, built progressively alongside my M1/M2 studies to gain the practical skills the job market expects — not coursework. Status per project is tracked honestly below.

---

## ✅ Delivered

### 🌾 agri-data-platform
[TO FILL: one line — what data it ingests, what it produces, who it is for]

- **Stack:** [TO FILL: tools actually used]
- **Highlights:** [TO FILL: 2–3 concrete points — data sources, pipeline steps, dashboard]
- **Repo:** [TO FILL: repo link]

### 📥 P1 — FCFA Exchange Rate Ingestion
Python pipeline that collects daily XOF/USD, XOF/EUR and XOF/CNY exchange rates, validates them and stores them as Parquet. API client with retry logic and structured logging, Pydantic validation.

- **Stack:** Python · REST API · Pydantic · Parquet
- **Repo:** [p1-fcfa-exchange-rate](https://github.com/Aliou-THIELO/p1-fcfa-exchange-rate)

### 💼 Xarala Talent Camp — Radar Emploi & Compétences (Summer 2026)
Team project (Squad Cayor, 5 members) building an automated radar of job offers and in-demand skills in Senegal, to help training providers, students and recruiters see what the market actually asks for. **Role: Data Lead (AI & Data Engineering lane).**

- **Collection:** daily automated scraping of 4 Senegalese job platforms, with a shared collector interface and `robots.txt` checks per source
- **AI extraction:** skills extracted from job descriptions with an LLM (Groq, Llama 3) and validated against a strict JSON schema with Pydantic
- **Embeddings:** multilingual sentence embeddings (384 dimensions) stored in Supabase (pgvector)
- **Ingestion:** validated offers sent to a FastAPI backend with duplicate detection
- **Quality and operations:** pytest suite (unit tests, mocked API tests, opt-in integration test), GitLab CI/CD, Discord notifications on pipeline success/failure
- **Team workflow:** Git flow with merge requests, code review by the project mentor, handover so a teammate can rerun the pipeline independently
- **Stack:** Python · BeautifulSoup · Pydantic · Groq API · sentence-transformers · FastAPI · Supabase/PostgreSQL · GitLab CI/CD · n8n *(the web application was built by teammates)*

---

## 🔨 In Progress — Main Pipeline: Data Engineering & MLOps

**One connected pipeline, from raw data to cloud production.**

| # | Project | Stack | Status |
|---|---|---|---|
| P1 | [📥 FCFA Exchange Rate Ingestion](https://github.com/Aliou-THIELO/p1-fcfa-exchange-rate) | Python · REST API · Pydantic · Parquet | ✅ Done |
| P2 | [🔄 Data Transformation Layer](https://github.com/Aliou-THIELO/p2-fcfa-dbt-transformation) | dbt (DuckDB for dev, PostgreSQL for prod) · 3-layer architecture | 🔨 In progress |
| — | 🔍 Exploratory Data Analysis | Streamlit | ⏳ Planned |
| P3 | ⚙️ Pipeline Orchestration | Apache Airflow · Docker | ⏳ Planned |
| — | 📊 Business Dashboard | Power BI (fed by the orchestrated, automated pipeline) | ⏳ Planned |
| P4 | 🤖 ML Model & Experiment Tracking | Scikit-learn · MLflow | ⏳ Planned |
| P5 | 🚀 Model Deployment API | FastAPI · Docker | ⏳ Planned |
| P6 | ☁️ End-to-End Cloud Pipeline | AWS S3 · Glue · Athena · Redshift | ⏳ Planned |

**The logic:** P1 feeds P2 → transformed data is explored via Streamlit (EDA: means, volatility, trends) for manual validation → P3 automates P1+P2, so the pipeline runs on a schedule rather than manual triggers → once automated, it feeds the Power BI business dashboard, reflecting a live pipeline rather than a manual snapshot → P4 (ML) is trained on the transformed data → P5 deploys P4 → P6 migrates the full pipeline to AWS, in preparation for the AWS Certified Data Engineer – Associate certification.

---

## 🧱 Roadmap — Big Data at Scale

**Planned: a pan-African e-commerce data platform (Airflow · Spark · Iceberg · dbt).**

The main pipeline above runs on real but low-volume data. To demonstrate Big Data tooling at a realistic scale, this project will run on an independently generated, high-volume simulated dataset, orchestrated end to end: Airflow → Spark → Iceberg → dbt.

This separation is deliberate: using Spark on a handful of daily rows would be technically unjustified. The project exists to show *when* and *why* these tools are used — not just that I can name them. It is scheduled after the main pipeline, once Data Engineering fundamentals (SQL, Python, the P1–P4 flow) are solidly in place.

---

## 🛠️ Tech Stack

**Used in delivered projects**

| Layer | Tools |
|---|---|
| Ingestion | Python · REST API · BeautifulSoup · Pydantic · Parquet |
| AI / NLP | Groq API (Llama 3) · sentence-transformers · pgvector |
| Storage & API | PostgreSQL (Supabase) · SQL · FastAPI (as ingestion target) |
| Testing & CI/CD | pytest · GitLab CI/CD |
| Notifications | n8n · Discord |
| Versioning | Git · GitHub · GitLab |

**Learning / on the roadmap**

| Layer | Tools |
|---|---|
| Transformation | dbt · DuckDB |
| Exploration & Visualization | Streamlit · Power BI |
| Orchestration | Apache Airflow · Docker |
| Big Data | Apache Spark (PySpark) · Apache Iceberg |
| ML & MLOps | Scikit-learn · MLflow · FastAPI (deployment) |
| Cloud | AWS S3 · Glue · Athena · Redshift |

---

## 🎯 Domains of Application

**Sector-neutral — applied so far to:**

- 🌾 Agricultural data — *agri-data-platform*
- 💼 Labour-market data (job offers, skills demand) — *Xarala Talent Camp*
- 📊 Financial data (FCFA exchange rates, WAEMU zone) — *P1 delivered, P2 to P6 in progress / planned*

**Open to:** fintech and banking, agriculture, health, environment, public sector.

**Roadmap:** ☁️ cloud data infrastructure on AWS (P6).

The ingestion and validation approach is domain-agnostic — the same pipeline structure applies equally well to health, agricultural, or public-sector data.

---

## 📈 Current Focus

- ✅ agri-data-platform — [TO FILL: final phase / delivered — one short line]
- ✅ Xarala Talent Camp — Radar Emploi & Compétences, internship completed
- 🔨 P2 — dbt transformation layer (models and tests in progress)
- 🔜 P3 — Airflow + Docker orchestration, then AWS Certified Data Engineer – Associate

## 📫 Let's Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Aliou%20THIELO-0077B5?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/aliou-thielo-815bba389)
[![Email](https://img.shields.io/badge/Email-thieloaliou25%40gmail.com-D14836?logo=gmail&logoColor=white)](mailto:thieloaliou25@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-Aliou--THIELO-181717?logo=github&logoColor=white)](https://github.com/Aliou-THIELO)

## 📫 Let's Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Aliou%20THIELO-0077B5?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/aliou-thielo-815bba389)
[![Email](https://img.shields.io/badge/Email-thieloaliou25%40gmail.com-D14836?logo=gmail&logoColor=white)](mailto:thieloaliou25@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-Aliou--THIELO-181717?logo=github&logoColor=white)](https://github.com/Aliou-THIELO)
