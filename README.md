# Telecom-Churn-analysis

> **Note:** This is a self-initiated portfolio project. The business scenario and stakeholder are fictional, and the data comes from a public dataset (IBM Telco Customer Churn on Kaggle).

![Dashboard Preview](images/dashboard_preview.png)
*(Replace with a screenshot of your dashboard)*

---

## 1. Project Overview

**Company (fictional):** ConnectPlus Telecom
**Stakeholder (fictional):** Priya Sharma, VP of Customer Retention
**My role:** Data Analyst

ConnectPlus Telecom is losing customers at a rate the leadership team finds concerning. Priya has asked for an analysis that explains **who is leaving, why they are leaving, and what the company can do to reduce churn.**

## 2. Business Question

> Which customers are most likely to churn, what factors drive churn, and what actions can reduce it?

**Success metric:** Identify the top churn drivers and recommend actions that could reduce churn by [X]% (e.g. 5%).

## 3. Key Questions Answered

1. What is the overall churn rate?
2. How does contract type affect churn?
3. Do new customers churn more than long-term customers?
4. Is there a relationship between monthly charges and churn?
5. Which services (internet type, tech support, etc.) are linked to churn?
6. Which payment methods have the highest churn?

## 4. Dataset

- **Source:** [IBM Telco Customer Churn - Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Size:** ~7,000 customers, 21 columns
- **Target variable:** `Churn` (Yes / No)
- **Key columns:** `tenure`, `Contract`, `MonthlyCharges`, `TotalCharges`, `InternetService`, `TechSupport`, `PaymentMethod`

## 5. Tools Used

| Stage | Tool |
|---|---|
| Data extraction and segmentation | SQL (MySQL / PostgreSQL / SQLite) |
| Cleaning, analysis, modeling | Python (pandas, NumPy, matplotlib, seaborn, scikit-learn) |
| Dashboard | Power BI / Tableau |
| Documentation and version control | Markdown, Git, GitHub |

## 6. Project Workflow

1. **Data loading:** imported the CSV into Python and SQL
2. **Data cleaning:**
   - Converted `TotalCharges` from text to numeric
   - Handled [X] blank values (new customers with tenure = 0)
   - Checked for duplicates and inconsistent categories
3. **Exploratory analysis:** compared churn across all key variables
4. **Segmentation:** grouped customers by tenure, contract, and charges
5. **Predictive model:** built [Logistic Regression / Random Forest] to predict churn
6. **Dashboard:** built an interactive dashboard with KPIs and filters
7. **Recommendations:** translated findings into business actions

## 7. Key Findings

> Replace the numbers below with your own results.

**Finding 1: Contract type is the strongest churn driver**
- Month-to-month customers churn at **42.71%**, versus **2.83%** for two-year contracts.
- *Why it matters:* short contracts make it easy for customers to leave.

**Finding 2: Early-tenure customers are most at risk**
- Customers in their first **12 months** show the highest churn.
- *Why it matters:* the onboarding period is where the company loses the most customers.

**Finding 3: Higher monthly charges are linked to higher churn**
- Customers paying above **$74.44** per month churn more often.
- *Why it matters:* price sensitivity is likely a factor, especially for fiber optic users.

**Finding 4: Customers without add-on support services churn more**
- Customers without Tech Support or Online Security churn at **[XX]%**.

**Finding 5: Payment method matters**
- Electronic check users show the highest churn at **45.29%**.

## 8. Model Performance (Optional)

| Metric | Score |
|---|---|
| Accuracy | [XX]% |
| Precision | [XX]% |
| Recall | [XX]% |
| ROC-AUC | [XX] |

**Top features driving churn:** [list the top 3-5 from your model]

## 9. Recommendations

| # | Recommendation | Target segment | Expected impact |
|---|---|---|---|
| 1 | Offer discounts to move customers to 1-2 year contracts | Month-to-month customers | Lower churn in the largest at-risk group |
| 2 | Launch a 90-day onboarding and check-in program | New customers (tenure < 6 months) | Reduce early-stage churn |
| 3 | Bundle free Tech Support / Online Security for a trial period | Customers without add-ons | Improve satisfaction and stickiness |
| 4 | Encourage auto-pay with a small incentive | Electronic check users | Reduce payment-related churn |

## 10. Dashboard

The dashboard includes:
- Overall churn rate and customer KPIs
- Churn by contract, tenure, services, and payment method
- Filters for customer segments

**Link:** [Add your Power BI / Tableau Public link here]

## 11. Repository Structure

```
telecom-churn-analysis/
├── data/
│   ├── raw/                  # original dataset
│   └── cleaned/              # cleaned dataset
├── notebooks/
│   └── churn_analysis.ipynb  # cleaning, EDA, modeling
├── sql/
│   └── segmentation_queries.sql
├── dashboard/
│   └── churn_dashboard.pbix  # or Tableau workbook
├── images/
│   └── dashboard_preview.png
├── presentation/
│   └── churn_summary.pdf     # short client-style deck
└── README.md
```

## 12. How to Run This Project

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/telecom-churn-analysis.git
   cd telecom-churn-analysis
   ```
2. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   ```
3. Open the notebook:
   ```bash
   jupyter notebook notebooks/churn_analysis.ipynb
   ```

## 13. Limitations and Next Steps

- The dataset is a snapshot, so it cannot show how churn changes over time.
- Customer satisfaction and call-center data are not included.
- **Next steps:** test additional models, add a customer lifetime value (CLV) analysis, and estimate the revenue impact of each recommendation.

## 14. About Me

**[Your Name]**
Aspiring Data Analyst | Completed the Deloitte and Cisco Data Analytics programs

- LinkedIn: [your link]
- GitHub: [your link]
- Email: [your email]
