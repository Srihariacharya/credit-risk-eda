# Credit Risk EDA — Python Project 🏦

## Overview
Exploratory Data Analysis on a real-world credit risk dataset to identify key factors that predict loan defaults. This project simulates the kind of analysis done by data analysts at banks, NBFCs and fintech companies in India.

---

## Dataset
- **Source:** Kaggle — laotse/credit-risk-dataset
- **Size:** 32,581 rows × 12 columns
- **Target Variable:** `loan_status` (0 = No Default, 1 = Default)

---

## Tools Used
- Python 3
- Pandas — data cleaning and analysis
- NumPy — numerical operations
- Matplotlib — static visualizations
- Seaborn — statistical visualizations
- Google Colab — development environment

---

## Project Structure
```
credit-risk-eda/
│
├── credit_risk_eda.ipynb       ← Main analysis notebook
├── univariate_analysis.png     ← Distribution charts
├── bivariate_analysis.png      ← Feature vs Default charts
├── correlation_heatmap.png     ← Correlation matrix
├── key_insights.png            ← Business insight charts
└── README.md
```

---

## What I Did

### Section 1 — Data Understanding
- Explored 32,581 loan records across 12 features
- Identified missing values in `loan_int_rate` and `person_emp_length`
- Checked data types and basic statistics

### Section 2 — Data Cleaning
- Removed outliers in age (> 100 years)
- Removed unrealistic employment lengths (> 60 years)
- Filled missing interest rates with median
- Filled missing employment lengths with median
- Removed duplicate records

### Section 3 — Univariate Analysis
- Plotted distribution of all numeric features
- Analyzed categorical breakdowns — home ownership, loan intent, loan grade
- Found overall default rate of ~21.8%

### Section 4 — Bivariate Analysis
- Compared each feature against loan_status (default vs no default)
- Found loan grade is the strongest predictor
- Found previous default history doubles the risk
- Found higher loan-to-income ratio = higher default probability

### Section 5 — Correlation Analysis
- Built correlation heatmap of all numeric features
- Found loan_percent_income has highest positive correlation with default
- Found person_income has negative correlation with default

### Section 6 — Key Visualizations
- Previous default history impact on current default rate
- Loan-to-income ratio buckets vs default rate

### Section 7 — Business Insights
- 5 actionable business insights with recommendations

---

## Key Findings

| Finding | Detail |
|---|---|
| Overall Default Rate | ~21.8% of borrowers defaulted |
| Strongest Predictor | Loan grade — Grade G has 60%+ default rate |
| Previous Default Impact | 2x higher risk for borrowers with default history |
| Income Effect | Lower income borrowers default more frequently |
| Loan-to-Income Risk | Loans exceeding 60% of income carry very high risk |

---

## Business Insights

**Insight 1 — Loan Grade is Critical**
Grade G loans have 60%+ default rate vs Grade A at under 5%. Cap loan amounts for Grade D-G customers.

**Insight 2 — Previous Default Doubles Risk**
Customers with previous default history are 2x more likely to default again. Require additional collateral from this segment.

**Insight 3 — Loan-to-Income Policy**
Set a maximum loan-to-income ratio of 40% as lending policy to reduce default risk significantly.

**Insight 4 — Income-Based Screening**
Lower income borrowers default significantly more. Implement stricter screening for income below median.

**Insight 5 — Loan Purpose Matters**
Debt consolidation loans show higher default rates. Prioritize education and medical loans which show lower default rates.

---

## Charts Built

1. Univariate distributions — 3×3 subplot grid
2. Bivariate analysis — features vs loan_status
3. Correlation heatmap
4. Previous default history vs current default rate
5. Loan-to-income ratio buckets vs default rate

---

## How to Run

1. Clone this repository
2. Download dataset from Kaggle: `laotse/credit-risk-dataset`
3. Open `credit_risk_eda.ipynb` in Google Colab
4. Upload `credit_risk_dataset.csv`
5. Run all cells

---

## Author
Data Analytics Portfolio Project — Week 4
