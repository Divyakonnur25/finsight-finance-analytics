# 💰 FinSight — Finance Transactions & Risk Analytics Dashboard

> End-to-end analytics project cleaning **50,000+ transactions** and **5,000+ customer records**, then visualizing spend, risk, and customer behavior in an interactive Power BI dashboard.

---

## 📌 Project Overview

FinSight analyzes financial transaction data to surface revenue trends, fee/tax patterns, and customer risk signals for a retail banking dataset. This project builds a full analytics pipeline — from raw data cleaning in Python to a 2-page interactive Power BI dashboard — to help stakeholders monitor transaction health across channels, segments, and geographies.

The dataset covers **15,000+ transactions** across **10 transaction types**, **5 customer segments**, and **28 states**, for the year 2024.

---

## 🚨 Key Findings

| Metric                  | Value             |
| ------------------------ | ----------------- |
| Total Transaction Amount | ₹135.62M           |
| Total Transactions       | 15,000             |
| Avg Transaction Value    | ₹9.02K              |
| Total Fees Collected     | ₹217.30K            |
| Total Tax Collected      | ₹39.14K              |
| Successful Transactions  | **85.05%**          |
| Failed Transactions      | 10.52%              |
| Pending Transactions     | 4.44%                |

### 🔍 Critical Insight

**Retail customers drive the majority of volume** — the Retail segment accounts for ₹74M of total transaction amount, more than 3x the next-largest segment (Premium, ₹26M). **Loan EMI (₹39.87M)** and **Transfer (₹35.69M)** are the two largest transaction types by value, together making up over half of total volume.

---

## 📊 Dashboard Pages

### Page 1 — Overview Analysis
- KPI cards: Total Amount, Total Transactions, Avg Transaction Value, Total Fees, Total Tax (with YoY change)
- Total Amount by Month (trend line)
- Total Amount by Transaction Status (donut: Success / Failed / Pending)
- Total Amount by Customer Segment (Retail, Premium, SME, Corporate, Wealth)
- Total Amount by State (top states by volume)
- Transaction Type Analysis (amount, fees, tax, count by type)
- Total Amount by Gender

### Page 2 — Transactions
- Full transaction-level table (Transaction ID, Date, Customer, Type, Status, Gender, Segment, State, Amount, Fees, Tax) with **drill-down** for record-level detail
- Filters: Year, Occupation, Category

---

## 🗂️ Folder Structure

```
finsight-finance-analytics/
│
├── README.md
├── Raw data/
│   ├── customers.csv
│   └── finance_transactions.csv
├── Cleaned data/
│   ├── customers_cleaned.csv
│   └── finance_transactions_cleaned.csv
├── Notebook/
│   └── Finance_analysis.ipynb
├── Dashboard/
│   └── Finance_analysis.pbix
└── Screenshort/
    ├── Overview.png
    └── Transaction.png
```

---

## 🛠️ Tech Stack

| Tool                       | Purpose                             |
| -------------------------- | ------------------------------------ |
| **Python** (Pandas, NumPy) | Data cleaning, deduplication, EDA    |
| **Power BI**               | Interactive dashboard, DAX measures  |
| **Jupyter Notebook**       | Data cleaning & preprocessing workflow |

---

## 🧹 Data Cleaning Highlights

- Removed duplicate transaction records (matched on `transaction_id`)
- Imputed missing `fee_amount` values using column mean
- Converted `transaction_date`, `date_of_birth`, and `join_date` to proper datetime format
- Standardized categorical fields (currency casing, transaction type, merchant category)

---

## 📷 Dashboard Screenshots

### Overview Analysis
[![Overview](https://github.com/Divyakonnur25/finsight-finance-analytics/raw/main/Screenshort/Overview.png)](/Divyakonnur25/finsight-finance-analytics/blob/main/Screenshort/Overview.png)

### Transactions
[![Transactions](https://github.com/Divyakonnur25/finsight-finance-analytics/raw/main/Screenshort/Transaction.png)](/Divyakonnur25/finsight-finance-analytics/blob/main/Screenshort/Transaction.png)

---

## 💡 Business Recommendations

1. **Investigate the 10.52% failed-transaction rate** — even a small reduction here directly recovers revenue and improves customer trust.
2. **Deepen Retail-segment engagement** — Retail drives 55% of total volume; targeted product offers here have outsized impact.
3. **Monitor Loan EMI and Transfer flows closely** — these two types alone represent ~56% of total transaction value and warrant dedicated risk monitoring.
4. **Review state concentration** — Maharashtra, Karnataka, and Gujarat together account for the largest share of volume; regional strategies could reduce over-reliance on top states.

---

## 🔄 Project Workflow

```
Raw Data
   ↓
Python (Pandas) — Cleaning & Preprocessing
   ↓
Power BI — Data Modeling & DAX Measures
   ↓
Dashboard & Insights
```

---

## 👩‍💻 Author

**Divya Raghavendra Konnur**
Data Analyst Intern | Computer Science Engineering

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://www.linkedin.com/in/divya-konnur-4982a3345) [![GitHub](https://img.shields.io/badge/GitHub-Divyakonnur25-black?logo=github)](https://github.com/Divyakonnur25)

---

## 📁 Related Projects

- [Counterfeit Intelligence Dashboard](https://github.com/Divyakonnur25/counterfeit-intelligence-dashboard) — fraud detection dashboard using Python, SQL, and Power BI
- [AttritionIQ](https://github.com/Divyakonnur25/AttritionIQ) — HR attrition analysis using Python, SQL, and Power BI

---

*Built as part of a self-directed data analytics portfolio. All data is synthetically generated for educational purposes.*
