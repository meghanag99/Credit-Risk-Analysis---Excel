# Consumer Credit Risk & Loan Default Analysis Dashboard

## Project Overview
This project analyzes a consumer loan portfolio to identify the key drivers of borrower default risk and uncover high-risk borrower segments. The analysis examines how borrower characteristics, loan affordability, credit grade, interest rate tiers, employment stability, and prior credit behavior influence loan repayment outcomes.

An interactive dashboard was built using **Microsoft Excel** to visualize patterns across the loan portfolio and enable exploration of borrower risk through multiple segmentation dimensions.

The objective of this project is to demonstrate how data analysis can support **credit risk assessment, underwriting decisions, and portfolio risk management** in consumer lending.

---

## Dataset Overview

The dataset contains historical records of consumer loans issued by a lending institution. Each row represents an individual borrower loan record, containing both borrower characteristics and loan attributes.

The dataset includes **32,409 loan observations**, capturing information related to borrower demographics, employment status, credit profile, and loan repayment outcomes.

---

## Data Cleaning and Preparation

Several preprocessing steps were performed to improve data quality and ensure reliable analysis.

### Duplicate Removal
Duplicate records were removed to ensure that each row represented a unique borrower loan record.

### Employment Length Validation
Certain records contained employment length values greater than the borrower’s age, which is logically inconsistent. These values were corrected by replacing them with the median employment length.

### Missing Interest Rate Handling
Missing interest rate values were imputed using the **median interest rate within each loan grade**, ensuring that replacement values remained consistent with borrower risk categories.

### Loan-to-Income Ratio Verification
The affordability variable **loan_percent_income** was verified and recalculated where necessary using: Loan Percent Income = Loan Amount / Borrower Income

## Key Portfolio Insights

### Overall Portfolio Health
The loan portfolio shows an **overall default rate of approximately 22%**, with **7,088 defaults out of 32,409 issued loans**. This indicates that roughly **one in five borrowers fails to repay their loan**, highlighting the importance of borrower risk segmentation.

---
### Key Findings Summary

| Risk Dimension | Segment | Default Rate |
|----------------|--------|-------------|
| Portfolio Health | Overall Loan Portfolio | ~22% |
| Credit Grade (Lowest Risk) | Grade A | ~10% |
| Credit Grade (Highest Risk) | Grade G | ~98% |
| Borrower Affordability (Lowest Risk) | Loan % Income (0–10%) | ~11% |
| Borrower Affordability (Highest Risk) | Loan % Income (50–60%) | ~78% |
| Interest Rate Tier (Lowest Risk) | 5–7% Interest Rate | ~8% |
| Interest Rate Tier (Highest Risk) | 21–23% Interest Rate | ~83% |
| Employment Stability (Lowest Risk) | 12–14 Years Employment | ~15% |
| Employment Stability (Highest Risk) | 0–2 Years Employment | ~27% |
| Credit History | Prior Default on File | Significantly Higher Default Risk |
| Borrower Housing Status | Renters | Higher Default Concentration |

### Credit Grade Risk Escalation

| Credit Grade | Default Rate |
|-------------|-------------|
| A | ~10% |
| B | ~16% |
| C | ~21% |
| D | ~59% |
| E | ~64% |
| F | ~71% |
| G | ~98% |

The analysis shows that credit grades **D through G represent significantly higher-risk borrower segments**, suggesting a substantial deterioration in borrower creditworthiness within these tiers.

---

### Borrower Affordability Risk

| Loan Percent Income | Default Rate |
|--------------------|-------------|
| 0–10% | ~11% |
| 10–20% | ~15% |
| 20–30% | ~21% |
| 30–40% | ~62% |
| 40–50% | ~73% |
| 50–60% | ~78% |

Default rates increase dramatically once borrower loan obligations exceed **30% of income**, indicating a critical affordability threshold.

---

### Interest Rate vs Risk Alignment
Higher interest rates are generally associated with higher default rates. This suggests that lenders apply **risk-based pricing**, charging higher rates to borrowers with higher perceived risk.

However, default rates remain extremely high in the highest interest rate brackets, indicating that pricing alone may not sufficiently offset borrower risk.

---

### Employment Stability

| Employment Length | Default Rate |
|------------------|-------------|
| 0–2 years | ~27% |
| 3–5 years | ~21% |
| 6–11 years | ~18% |
| 12–20 years | ~15–16% |

Borrowers with longer employment tenure demonstrate stronger repayment reliability.

---

### Prior Default History
Borrowers with previous credit defaults demonstrate significantly higher default rates compared to borrowers without prior defaults.

Past credit behavior remains one of the strongest indicators of future repayment behavior.

---

### Risk Interaction Analysis
The heatmap analysis reveals that **default risk increases significantly when multiple risk factors overlap**, particularly:

- low credit grades
- high loan-to-income ratios

Borrowers combining poor credit quality with high debt burden represent the most vulnerable segments in the portfolio.

## Dashboard Overview

An interactive Excel dashboard was developed to visualize key drivers of loan default risk across the portfolio. The dashboard summarizes portfolio performance using KPI cards and multiple charts that analyze borrower risk across credit grade, loan-to-income ratio, interest rate tiers, employment stability, home ownership status, and loan purpose.

Interactive slicers allow users to filter the data dynamically, enabling deeper exploration of borrower segments and their default behavior. A heatmap is included to highlight how default concentration changes when multiple risk factors, such as credit grade and debt burden, interact.

The dashboard provides a clear visual overview of portfolio risk and helps identify high-risk borrower segments that may require stricter underwriting or pricing adjustments.

## Strategic Recommendations

Based on the findings from this analysis, several strategies could help improve portfolio risk management.

### Strengthen Underwriting for High-Risk Credit Grades
Loan approvals for borrowers in **Grades D–G** should be reviewed more carefully due to significantly elevated default risk.

### Introduce Loan-to-Income Thresholds
Borrowers allocating more than **30% of income toward loan repayment** demonstrate significantly higher default risk. Introducing affordability thresholds may improve loan performance.

### Incorporate Employment Stability into Risk Models
Employment tenure should be incorporated into borrower risk scoring models as a proxy for income stability.

### Monitor Borrowers with Prior Defaults
Borrowers with previous credit defaults should be subject to enhanced risk monitoring and stricter lending criteria.

## Assumptions and Limitations

1. Dataset is simulated for analytical demonstration purposes.
2. Macroeconomic variables were not included.

#### Conclusion

This analysis demonstrates how borrower credit quality, affordability, employment stability, and prior credit behavior influence loan repayment outcomes. By identifying the key drivers of default risk, financial institutions can improve underwriting strategies, optimize risk-based pricing, and better manage overall portfolio exposure.
