# 🛡️ Project Shield & Scale
## iGaming Fraud Intelligence & Payments Operations Analytics

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.0-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Domain](https://img.shields.io/badge/Domain-Payments%20%7C%20Fraud%20%7C%20iGaming-16A34A?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Complete-success?style=for-the-badge)

**End-to-end payments intelligence pipeline on 20,000 iGaming transactions**  
*Fraud detection · Entity linking · Revenue recovery modelling · Provider benchmarking*

[📓 Open Notebook](./Fraud_and_Monitoring(Project_Shield_and_Scale).ipynb) · [📊 View Dataset](./igaming_payments_20k.csv) · [🔗 Live Data View](https://docs.google.com/spreadsheets/d/1UayaGCyMndqBl9BxQuy2Yniw_sQHZqNIfcm9oEYhUKk/edit?usp=sharing)

</div>

---

## 📌 What This Project Does

Project Shield & Scale is a **production-style fraud and payments intelligence pipeline** built to answer the questions a real payments operations team faces daily:

> *"Which providers are generating the most fraud exposure? Are we processing revenue from compromised accounts? How much money are we losing to technical failures — and where?"*

The analysis covers **four analytical workstreams** that mirror real fraud and payments ops workflows used in fintech and iGaming operators.

---

## 🎯 Key Results

| Finding | Value |
|---------|-------|
| Transactions analysed | **20,000** |
| Fraud-suspected transactions identified | See notebook |
| Revenue flowing through flagged devices | Quantified per provider |
| Multi-accounting clusters detected | Entity-linked via device ID + IP |
| Revenue leakage from technical failures | Broken down by failure reason |
| Providers benchmarked | By success rate, corridor, time-of-day |
| High-risk corridors identified | Country × Provider combinations |

> Full quantified findings are inside the notebook with executive-ready charts.

---

## 🏗️ Architecture

```
igaming_payments_20k.csv  (20,000 transactions)
        │
        ▼
┌─────────────────────────────────────────────┐
│           ETL & Data Quality Layer           │
│  Google Sheets → SQLite (automated)          │
│  Data assertions · Schema validation         │
└──────────────────┬──────────────────────────┘
                   │
        ┌──────────┴──────────┐
        ▼                     ▼
┌───────────────┐    ┌─────────────────────┐
│  SQL Engine   │    │   Python Analytics  │
│  (SQLite)     │    │   (Pandas / Seaborn)│
│               │    │                     │
│ Aggregations  │    │ Entity linking      │
│ KPI queries   │    │ Velocity analysis   │
│ Corridor maps │    │ ML anomaly scoring  │
└───────┬───────┘    └──────────┬──────────┘
        └──────────┬────────────┘
                   ▼
        ┌──────────────────────┐
        │   4 Analytical       │
        │   Workstreams        │
        │                      │
        │  WS1: Fraud Risk     │
        │  WS2: Entity Intel   │
        │  WS3: Ops Health     │
        │  WS4: Decision Supp. │
        └──────────┬───────────┘
                   ▼
        Executive-ready charts + findings
```

---

## 📊 Dashboard Preview

### Fraud Detection Overview
![Fraud Detection Dashboard](./shield_and_scale_images/fraud_detection_overview.png)

### Entity Intelligence — Multi-Accounting Detection
![Entity Intelligence](./shield_and_scale_images/entity_intelligence.png)

### Provider Performance Benchmarking
![Provider Performance](./shield_and_scale_images/provider_performance.png)

### Revenue Recovery Analysis
![Revenue Recovery](./shield_and_scale_images/revenue_recovery.png)

> *All visualisations are generated inside the notebook and designed to be executive-readable.*

---

## 🔬 Analytical Workstreams

### Workstream 1 — Fraud Risk Deep Dive 🚨

**Question:** Which providers, countries, and channels pose the highest fraud risk?

**Methods:**
- Fraud rate calculation by provider, country, and channel
- Transaction value distribution analysis (low-value card testing vs high-value attacks)
- High-risk corridor mapping (Country × Provider pairs)
- Fraud concentration vs volume analysis

**Outputs:**
- Ranked provider fraud risk table
- High-risk corridor heatmap
- Fraud rate benchmarks per channel

---

### Workstream 2 — Entity Intelligence & Multi-Accounting 🔗

**Question:** Are fraudsters operating multiple accounts linked through shared infrastructure?

**Methods:**
- Device ID → User ID mapping (many-to-many relationship analysis)
- IP address reuse detection across user accounts
- Success-after-failure audit: revenue from users who previously had fraud-suspected transactions
- Velocity burst detection: abnormal transaction frequency clustering

**Outputs:**
- Multi-accounting cluster map
- Quantified revenue at risk from flagged device hardware
- Velocity anomaly flags per user/device group

---

### Workstream 3 — Operational Health & Revenue Recovery 💰

**Question:** How much revenue is lost to technical failures, and where?

**Methods:**
- Failure reason breakdown (timeout vs provider error vs user error)
- Provider performance by time-of-day (peak vs off-peak degradation)
- Currency success rate comparison across corridors
- Net recovery scenario modelling by provider

**Outputs:**
- Revenue leakage quantification by failure category
- Provider disable/enable ROI model
- Currency corridor performance ranking

---

### Workstream 4 — Decision Support Intelligence 🎯

**Question:** If we had to act today, which single change would save the most money?

**Methods:**
- Comparative impact analysis across providers, channels, and corridors
- Risk-adjusted revenue ranking (revenue × fraud rate)
- Provider substitution scenario modelling

**Outputs:**
- Ranked action recommendations with estimated financial impact
- Provider risk-adjusted revenue scorecard
- Executive decision brief

---

## 🗂️ Repository Structure

```
payments-intelligence/
│
├── Fraud_and_Monitoring(Project_Shield_and_Scale).ipynb  ← Main analysis
├── igaming_payments_20k.csv                               ← Dataset (20K rows)
├── README.md                                              ← This file
├── requirements.txt                                       ← Python dependencies
│
└── shield_and_scale_images/                               ← Dashboard exports
    ├── fraud_detection_overview.png
    ├── entity_intelligence.png
    ├── provider_performance.png
    └── revenue_recovery.png
```

---

## 🧰 Tech Stack

| Tool | Purpose |
|------|---------|
| **Python 3.10+** | Core analytics language |
| **Pandas** | Data manipulation, aggregation, KPI calculation |
| **SQLite + SQL** | ETL pipeline, structured queries, KPI extraction |
| **Matplotlib / Seaborn** | Executive-ready visualisations |
| **Jupyter Notebook** | Analysis environment and storytelling |
| **Google Sheets** | Initial data inspection and ETL source |

---

## 🚀 How to Run

### Option A — Google Colab (recommended, no install)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mutumaian29/payments-intelligence/blob/main/Fraud_and_Monitoring(Project_Shield_and_Scale).ipynb)

1. Click the badge above
2. Runtime → Run all

### Option B — Local

```bash
# Clone the repository
git clone https://github.com/mutumaian29/payments-intelligence.git
cd payments-intelligence

# Install dependencies
pip install -r requirements.txt

# Launch notebook
jupyter notebook "Fraud_and_Monitoring(Project_Shield_and_Scale).ipynb"
```

---

## 📦 Dataset

| Field | Detail |
|-------|--------|
| **File** | `igaming_payments_20k.csv` |
| **Rows** | 20,000 transaction attempts |
| **Domain** | iGaming payments |
| **Granularity** | Transaction-level |
| **PII** | None — fully anonymised |

**Key columns:**

| Column | Description |
|--------|-------------|
| `transaction_id` | Unique transaction reference |
| `user_id` | Anonymised user identifier |
| `device_id` | Device fingerprint (for entity linking) |
| `ip_address` | IP address (for entity linking) |
| `provider` | Payment provider name |
| `currency` | Transaction currency |
| `country` | Transaction origin country |
| `transaction_type` | Deposit or withdrawal |
| `status` | `success` / `failed` / `fraud_suspected` |
| `failure_reason` | Root cause of failure (timeouts, errors, etc.) |
| `amount` | Transaction value |
| `timestamp` | Transaction datetime |

---

## 💡 Why This Project Exists

This project was built to demonstrate payments operations and fraud intelligence skills in a realistic, domain-specific context — not as a generic data science exercise.

Every analytical decision mirrors what a real **fraud analyst**, **payments operations specialist**, or **risk analytics team** would prioritise:

- Focus on **business impact** (revenue exposure, not just anomaly counts)
- Think in **operational workflows** (provider routing, corridor management)
- Frame findings as **decisions** (which provider to disable, which accounts to flag)
- Build for **executive audiences** (visual clarity, plain-English summaries)

---

## 🗺️ Roadmap

- [x] Phase 1: ETL pipeline + data quality
- [x] Phase 2: Fraud risk workstream
- [x] Phase 3: Entity intelligence workstream
- [x] Phase 4: Operational health workstream
- [x] Phase 5: Decision support workstream
- [ ] Phase 6: Chargeback and dispute integration
- [ ] Phase 7: Real-time alerting logic
- [ ] Phase 8: ML fraud scoring (Isolation Forest)
- [ ] Phase 9: Reconciliation and settlement workstream

---

## 👤 Author

**Ian Mutuma** — Payments Operations Specialist | iGaming & Fintech

- 📧 mutumian29@gmail.com
- 💼 [LinkedIn](https://linkedin.com/in/ian-mutuma-3639bb280)
- 🐙 [GitHub](https://github.com/mutumaian29)

*Focus areas: Payments analytics · Fraud monitoring · Reconciliation · AML · Risk intelligence*

---

<div align="center">

*If this project was useful, a ⭐ is appreciated.*

**[🔝 Back to top](#️-project-shield--scale)**

</div>
