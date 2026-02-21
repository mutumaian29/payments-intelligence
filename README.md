# Project Shield & Scale  
### iGaming Fraud Monitoring & Payments Operations Analytics

## 📌 Overview
Project **Shield & Scale** is an end-to-end payments analytics project focused on **fraud detection, transaction monitoring, and operational health** within an iGaming environment.

As the business scales across multiple regions, payment providers, and currencies, the risk of **fraud syndicates, multi-accounting, and technical revenue leakage** increases. This project demonstrates how transaction-level data can be transformed into **actionable business intelligence** using SQL, Python, and data visualization.

The analysis is designed to mirror **real-world payments monitoring workflows** used by fintechs and iGaming operators.

---

## 🎯 Business Objectives
The project answers four core business questions:

1. **Fraud Risk**
   - Which providers, countries, and channels pose the highest fraud risk?
   - Are fraudsters testing small amounts or targeting high-value transactions?

2. **Entity Intelligence**
   - Are multiple user accounts linked through shared devices or IP addresses?
   - How much “successful” revenue came from previously flagged devices?

3. **Operational Health**
   - How much revenue is lost due to technical failures (timeouts, provider errors)?
   - Are certain providers or currencies underperforming?

4. **Decision Support**
   - If we had to disable one provider, channel, or corridor to reduce losses, which would save the most money?

---

## 🗂 Dataset
- **Size:** 20,000 transaction attempts  
- **Type:** Simulated but realistic iGaming payments data  
- **Granularity:** Transaction-level  
- **Key Fields:**
  - `transaction_id`
  - `user_id`
  - `provider`
  - `currency`
  - `country`
  - `transaction_type` (deposit / withdrawal)
  - `status` (success / failed / fraud_suspected)
  - `failure_reason`
  - `device_id`
  - `ip_address`
  - `timestamp`
  - `amount`

> ⚠️ No personally identifiable information (PII) is included.

---

## 🛠 Tools & Technologies
- **SQL (SQLite)** – data filtering, aggregation, KPI calculations  
- **Python**
  - Pandas – data manipulation & analytics
  - Matplotlib / Seaborn – visualizations
- **Jupyter Notebook** – analysis & storytelling
- **Google Sheets** – initial data inspection & validation
- **GitHub** – version control & portfolio presentation

---

## 🧱 Project Structure

### 1️⃣ Data Cleaning & Validation
- Removed invalid transactions (negative amounts, missing providers, invalid statuses)
- Validated data quality using Python assertions
- Ensured clean dataset for downstream analysis

---

### 2️⃣ Workstream 1: Fraud & High-Risk Deep Dive
**Key Analyses**
- Fraud rate by provider and country
- Transaction value analysis (low-value testing vs high-value attacks)
- Identification of high-risk corridors

**Outcome**
- Clear prioritization of providers and regions contributing most to fraud exposure

---

### 3️⃣ Workstream 2: Entity Intelligence & Multi-Accounting
**Key Analyses**
- Device IDs linked to multiple user accounts
- IP addresses reused across users
- “Success-after-failure” audit to quantify at-risk revenue
- Transaction velocity analysis (burst behavior)

**Outcome**
- Quantification of revenue flowing through previously flagged devices
- Identification of coordinated fraud patterns

---

### 4️⃣ Workstream 3: Operational Health & Revenue Recovery
**Key Analyses**
- Breakdown of technical failures (timeouts, provider errors)
- Provider performance by time-of-day
- Success rate comparison across currencies

**Outcome**
- Estimated revenue loss due to technical and provider-side issues
- Clear opportunities for provider optimization

---

## 📊 Visualizations
The notebook includes:
- Fraud rate by provider (bar charts)
- Transaction volume by provider
- High-risk device and IP analysis
- Revenue loss by failure reason
- Currency success rate comparison

All charts are designed to be **executive-readable** and portfolio-ready.

---

## 📈 Key Insights (Executive Summary)
- A small number of providers account for a disproportionate share of fraud risk
- Multi-accounting via shared devices represents a significant vulnerability
- A non-trivial portion of “successful” revenue originates from previously flagged hardware
- Technical failures (timeouts and provider errors) result in measurable revenue leakage
- Certain currencies exhibit consistently lower net success rates, indicating routing or provider inefficiencies

---

## 🚧 Limitations
- Dataset is simulated (no real chargeback confirmations)
- No machine learning fraud scoring applied
- Time-based analysis limited by dataset scope

These limitations were intentional to focus on **core payments analytics fundamentals**.

---

## 🚀 Next Steps
- Extend analysis to **reconciliation workflows**
- Introduce chargeback and dispute data
- Add alerting logic for real-time monitoring
- Compare pre- and post-mitigation fraud exposure

---

## 👤 Author
**Ian Mutuma**  
Payments Operations Specialist  
Focus areas: Payments analytics, fraud monitoring, reconciliation, risk analysis  

---

## 📎 How to Run
1. Clone the repository  
2. Open the notebook in Jupyter or Google Colab  
3. Install required Python packages (`pandas`, `matplotlib`, `seaborn`)  
4. Run all cells top to bottom  

---

⭐ *If you find this project useful, feel free to star the repository.*
