# Credit Risk Analysis

**Author**: Om Pawar  
**Project Type**: Exploratory Data Analysis (EDA)  
**Domain**: Finance / Lending / Risk Mitigation

## 📌 Problem Statement

The goal of this project is to perform a comprehensive analysis of loan application data to identify the key patterns and factors influencing loan defaults. Based on these insights, strategies are developed to mitigate credit risk in the lending process.

---

## 🗂️ Dataset Overview

The analysis is based on two key datasets:

- `application_data.csv`  
  - Rows: 307,511  
  - Columns: 122  

- `previous_application.csv`  
  - Rows: 1,670,214  
  - Columns: 37  

**Note:** More than 40% of the columns in `application_data.csv` had missing values, mostly statistical aggregates (mean, median, mode), and were dropped from the analysis.

---

## 🔍 Exploratory Data Analysis (EDA)

### 1. Data Imbalance
- Target variable is highly imbalanced.
- Separate DataFrames were created for `TARGET = 0` (non-defaulters) and `TARGET = 1` (defaulters).

### 2. Univariate Analysis
- **Cash Loans**: Higher default risk compared to revolving loans.
- **Revolving Loans**: Lower percentage of default.

### 3. Outlier & Age Distribution
- Median age: 40–50 years.
- Age range: 20 to 70 years (no extreme outliers).
- Older applicants show higher financial stability.

### 4. Education & Credit Risk
- 71% have Secondary education; higher defaults.
- Higher education applicants have fewer defaults and higher approval rates.

### 5. Bivariate Analysis
- Stable income types (e.g., Pensioner, Commercial Associate) show lower default rates.
- Unemployed and Students have higher default rates.

### 6. Correlation Insights
- No strong multicollinearity.
- Work phone and email presence have weak correlations with target outcome.

---

## ✅ Key Indicators of Repayers

| Factor | Insight |
|--------|---------|
| `NAME_EDUCATION_TYPE` | Academic degree = low default |
| `NAME_INCOME_TYPE` | Businessmen, Students = no default |
| `DAYS_BIRTH` | Age > 50 = lower risk |
| `DAYS_EMPLOYED` | > 40 years = <1% default rate |
| `AMT_INCOME_TOTAL` | > ₹700,000 = low default |
| `CNT_CHILDREN` | 0–2 = more likely to repay |

---

## ❌ Key Indicators of Defaulters

| Factor | Insight |
|--------|---------|
| `CODE_GENDER` | Males have higher defaults |
| `NAME_FAMILY_STATUS` | Single/Civil marriage = high risk |
| `OCCUPATION_TYPE` | Drivers, Laborers, Waiters = high risk |
| `ORGANIZATION_TYPE` | Transport type 3, Industry type 13 = high defaults |
| `DAYS_BIRTH` | Age 20–40 = higher probability of default |
| `CNT_CHILDREN` | ≥9 children = 100% default |

---

## 💡 Suggestions

- Track reasons for cancellation and rejections — many of these clients became successful repayers later.
- Leverage education, employment history, and age as strong features in credit scoring models.
- Consider conditional interest rate offers for high-risk segments.

---

## 📁 Project Files

- `CreditRiskAnalysis.ipynb`: Jupyter Notebook with complete code and visualizations.
- `Datasets/`: Contains `application_data.csv`, `previous_application.csv` and `columns_description.csv`.
- `CreditRiskAnalysis_InsightsAndSuggestions.pdf`: PDF report with summarized findings.

---

## 📬 Contact

**Om Pawar**  
📧 Email: [pawarom14112002@gmail.com]  
📍 Location: Mumbai, India  
🔗 [LinkedIn](https://www.linkedin.com/in/pawarom14)

---

## 📜 License

This project is for educational and research purposes only.

