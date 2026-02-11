# Credit Risk Analysis - Case Study

[![Python](https://img.shields.io/badge/Python-3.7%2B-blue)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

## 📌 Project Overview

The **Credit Risk Analysis Case Study** addresses a critical challenge in the **banking and finance sector**: minimizing financial loss due to loan defaults. This comprehensive analysis uses **Exploratory Data Analysis (EDA)** and **Statistical Hypothesis Testing** to identify patterns in consumer attributes and loan characteristics that indicate higher probability of default.

By leveraging data-driven insights, financial institutions can optimize lending decisions, reduce portfolio risk, and improve profitability.

### Business Problem
When a customer applies for a loan, the bank must decide:
- Should we approve this application?
- What interest rate should we charge?
- What credit limit should we offer?

Making the wrong decision can result in:
- **Approving risky customers** → Financial losses from defaults
- **Rejecting good customers** → Lost business opportunities

This analysis helps answer: **What factors predict loan defaults?**

---

## 🎯 Key Findings

### ✅ Overall Performance
- **Default Rate:** 8.1% (aligned with industry standard of 8%)
- **Dataset Size:** 307,511 loan applications analyzed
- **Statistical Validation:** All findings validated through hypothesis testing (p < 0.05)

### 🔍 Strongest Predictors of Default
1. **External Credit Scores (EXT_SOURCE)** - Most powerful predictor (correlation: -0.16)
2. **Previous Loan Rejections** - Customers with past rejections default significantly more
3. **Occupation Type** - Laborers, drivers have higher risk; professionals have lower risk
4. **Housing Stability** - Homeowners default less than renters
5. **Education Level** - Higher education correlates with better repayment

### ❌ Non-Predictive Factors
- **Income Level** - Does NOT significantly predict default (p = 0.98)
- **Loan Amount** - Large loans are not necessarily riskier

---

## 📊 Analysis Components

### 1. Exploratory Data Analysis (EDA)
- **Univariate Analysis:** Distribution of age, income, credit amounts, employment
- **Bivariate Analysis:** Relationships between features and default status
- **Multivariate Analysis:** Interaction effects between multiple variables
- **Correlation Analysis:** Identifying strongest numerical predictors

### 2. Statistical Hypothesis Testing
Five rigorous statistical tests performed:

| Test | Research Question | Result | P-value |
|------|------------------|---------|---------|
| Two-Sample t-test | Income difference between groups? | Not significant | 0.98 |
| Chi-Square Test | Gender affects default? | Significant | < 0.001 |
| Chi-Square Test | Education affects default? | Significant | < 0.001 |
| Proportion Z-Test | Previous rejections predict default? | Highly significant | < 0.001 |
| Proportion Z-Test | Default rate vs. industry benchmark? | Aligned | 0.069 |

### 3. Business Recommendations
- Prioritize external credit scores in decision models
- Flag customers with previous loan rejections
- Apply occupation-based risk segmentation
- Consider housing stability as a risk factor
- Develop predictive machine learning models

---

## 🛠️ Technologies Used

- **Python 3.7+**
- **Data Manipulation:** `pandas`, `numpy`
- **Visualization:** `matplotlib`, `seaborn`
- **Statistical Analysis:** `scipy`, `statsmodels`
- **Document Generation:** `python-docx`
- **Environment:** Jupyter Notebook

---

## 📂 Repository Structure

```
credit-risk-analysis/
│
├── Credit Risk Analysis - Case Study.ipynb    # Main analysis notebook
├── Credit_Risk_Analysis_Presentation_Report.docx  # Executive presentation
├── README.md                                   # This file
├── LICENSE                                     # MIT License
├── requirements.txt                            # Python dependencies
├── .gitignore                                  # Git ignore rules
│
└── Data Files (not included in repo):
    ├── credit_risk_applicants.csv              # Main dataset (307K rows)
    └── credit_risk_previous_loans.csv          # Historical data (1.67M rows)
```

---

## 📂 Dataset Information

### Primary Dataset: `credit_risk_applicants.csv`
- **Size:** 307,511 rows × 122 columns
- **Description:** Current loan applications with customer demographics and financial info
- **Key Variables:**
  - Demographics: Age, Gender, Education, Family Status
  - Financial: Income, Credit Amount, Employment Duration
  - Housing: Housing Type, Region
  - Target: `TARGET` (0 = Repaid, 1 = Defaulted)

### Secondary Dataset: `credit_risk_previous_loans.csv`
- **Size:** 1,670,214 rows × 37 columns
- **Description:** Historical loan application records
- **Purpose:** Used to create aggregated features (previous rejections, loan count)

> **⚠️ Note:** Dataset files are **not included** in this repository due to size. You must obtain the data separately to run the notebook.

---

## 📄 Deliverables

### 1. Jupyter Notebook
Complete analysis with:
- Data loading and exploration
- Univariate, bivariate, and multivariate analysis
- Statistical hypothesis testing
- Visualizations and insights
- Key findings and conclusions

### 2. Presentation Report (DOCX)
Professional executive summary including:
- Business context and objectives
- Key EDA insights
- Driver variables of default
- Statistical test results
- Actionable business recommendations
- Implementation roadmap

---

