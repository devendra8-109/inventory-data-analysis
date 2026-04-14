# 🏭 Vendor Performance & Supply Chain Risk Analysis

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![SQL](https://img.shields.io/badge/SQL-MySQL-orange?logo=mysql)
![PowerBI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow?logo=powerbi)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

> **Analysed 1M+ procurement and inventory records to uncover $2.71M in working capital inefficiency and critical supply chain risk — delivering actionable recommendations for vendor diversification and pricing optimisation.**

---

## 📌 Problem Statement

Organizations with large supplier networks often struggle to identify which vendors are underperforming, where inventory is getting stuck, and how concentrated their supply chain risk actually is. Without data-driven visibility, procurement decisions are made on assumptions rather than evidence.

This project simulates a real-world procurement analytics scenario to answer three business questions:

1. Which vendors are underperforming on margins and delivery efficiency?
2. How much capital is locked in slow-moving inventory — and where?
3. How concentrated is the supply chain risk, and what does that mean for the business?

---

## 📊 Key Business Findings

| Insight | Value |
|---|---|
| 💰 Slow-moving inventory identified | **$2.71M** |
| ⚠️ Procurement dependency on top vendors | **65%+** |
| 📉 Profit margin gap (high vs low vendors) | Statistically significant (p < 0.05) |
| 📦 Total records analysed | **1M+** |

---

## 🛠️ Tools & Technologies

| Layer | Tools Used |
|---|---|
| Data Cleaning & EDA | Python (Pandas, NumPy, Matplotlib, Seaborn) |
| Statistical Testing | SciPy (t-tests, hypothesis testing) |
| Data Querying & Profiling | SQL (Joins, CTEs, Window Functions, Subqueries) |
| ETL Pipeline | Python (extract → clean → transform → load) |
| Reporting & Dashboard | Power BI (DAX, Data Modelling, KPI Design) |

---

## 🗂️ Project Structure

```
vendor-performance-analysis/
│
├── data/
│   ├── raw/                        # Original procurement & inventory files
│   └── cleaned/                    # Post-ETL cleaned datasets
│
├── notebooks/
│   ├── 01_data_cleaning.ipynb      # ETL pipeline — cleaning & transformation
│   ├── 02_eda.ipynb                # Exploratory data analysis & profiling
│   ├── 03_vendor_analysis.ipynb    # Vendor KPI analysis & scoring
│   ├── 04_inventory_analysis.ipynb # Slow-moving inventory detection
│   └── 05_hypothesis_testing.ipynb # Statistical comparison of vendor margins
│
├── sql/
│   ├── vendor_kpi_queries.sql      # KPI extraction queries
│   ├── inventory_profiling.sql     # Inventory data profiling queries
│   └── supply_chain_risk.sql       # Vendor dependency & risk queries
│
├── dashboard/
│   └── vendor_dashboard.pbix       # Power BI dashboard file
│
├── reports/
│   └── findings_summary.pdf        # Key findings & recommendations
│
└── README.md
```

---

## ⚙️ ETL Pipeline

```
Raw Data (CSV/Excel)
      ↓
Extract — Load raw procurement & inventory files using Pandas
      ↓
Transform — Handle nulls, fix data types, standardise vendor names,
            remove duplicates, engineer features (inventory age, margin %)
      ↓
Load — Export cleaned data to structured schema for SQL querying & Power BI
```

---

## 🔍 Analysis Breakdown

### 1. Vendor Performance Scoring
- Scored each vendor on margin %, purchase frequency, and order consistency
- Identified top and bottom quartile vendors using SQL window functions (RANK, NTILE)
- Visualised vendor scorecards in Power BI with drill-through capability

### 2. Slow-Moving Inventory Detection
- Flagged inventory items with zero or low movement over 90+ days
- Quantified financial impact: **$2.71M** locked in non-moving stock
- Broke down by product category to prioritise clearance actions

### 3. Hypothesis Testing — Margin Comparison
- **Null Hypothesis (H₀):** No significant difference in profit margins between high and low performing vendors
- **Test Used:** Independent samples t-test (SciPy)
- **Result:** p-value < 0.05 → Rejected H₀ — margin difference is statistically significant
- **Implication:** High-performing vendors deliver meaningfully better margins, supporting selective contract renewal

### 4. Supply Chain Risk Assessment
- Calculated procurement concentration: top vendors account for **65%+** of total purchase value
- Modelled impact of losing a single top vendor on supply continuity
- Recommended vendor diversification threshold to reduce single-point-of-failure risk

---

## 📈 Power BI Dashboard

The dashboard includes:
- **Vendor Scorecard** — margin %, purchase volume, performance rank
- **Inventory Aging Report** — slow-moving items by category and value
- **Supply Chain Risk View** — vendor concentration heatmap
- **KPI Summary** — total spend, avg margin, inventory turnover rate

---

## 💡 Business Recommendations

1. **Vendor Diversification** — Reduce top-5 vendor dependency from 65% to below 45% over 2 quarters
2. **Inventory Clearance** — Initiate discount or liquidation strategy for $2.71M slow-moving stock
3. **Contract Renegotiation** — Use margin analysis findings to renegotiate terms with bottom-quartile vendors
4. **Reorder Policy** — Set data-driven reorder thresholds to prevent future inventory pile-up

---

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/devendra8-109/vendor-performance-analysis.git

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run notebooks in order
jupyter notebook notebooks/01_data_cleaning.ipynb
```

**Requirements:**
```
pandas
numpy
matplotlib
seaborn
scipy
jupyter
```

---

## 👤 Author

**Devendra Chouhan**
MSc Data Science — DAVV, Indore
📧 devendra8chouhan@gmail.com
🔗 [LinkedIn](https://linkedin.com/in/devendra-chouhan-b9542b203)
