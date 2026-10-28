# Customer Experience Analytics — Churn & Retention Analysis

This project analyzes customer churn at a telecommunications company to identify customer segments associated with higher cancellation rates and explore how machine learning can support retention strategies.

The analysis combines exploratory data analysis, customer segmentation, and LightGBM classification, with an emphasis on actionable business insights and transparent model evaluation.

## Business Objectives

- Identify customer segments with higher churn rates.

- Explore relationships between churn, contract types, internet services, and payment methods.

- Evaluate machine learning models for retrospective churn classification.

- Provide data-driven recommendations to support customer retention.

## Dataset

The dataset contains 7,043 customer records, including contract details, subscribed services, billing information, and demographic characteristics.

The overall observed churn rate is 26.54%.

## Dataset Access & Reproducibility

This project uses the Interconnect telecommunications customer dataset provided as part of the TripleTen Data Science program.

The original dataset is not included in this repository because its redistribution permissions have not been verified.

The Jupyter Notebook contains the analysis code, executed outputs, visualizations, model evaluation results, and business recommendations, allowing reviewers to examine the methodology and findings without downloading the original data.

To reproduce the analysis, authorized users must obtain the original dataset through their course materials and place the following files inside data/raw/:

contract.csv

internet.csv

personal.csv

phone.csv

## Tools & Technologies

Python · Pandas · NumPy · Matplotlib · Seaborn · Scikit-learn · LightGBM · Jupyter Notebook

## Key Findings

Month-to-month contracts: 42.7% churn, compared with 11.3% for one-year contracts and 2.8% for two-year contracts.

Fiber optic customers: 41.9% churn.

Electronic check payments: 45.3% churn.

Customer characteristics: Churned customers generally have higher monthly charges and shorter estimated tenure.

## Predictive Modeling Results

Two LightGBM models were evaluated:

| Metric | Initial Model | Adjusted Model |
|:---|---:|---:|
| ROC-AUC | 0.9344 | 0.8110 |
| Recall | 0.7388 | 0.4989 |
| Precision | 0.8712 | 0.5825 |
| F1-score | 0.7995 | 0.5375 |

The adjusted model excludes TotalCharges and TenureMonths to reduce dependence on potentially problematic temporal information.

The adjusted model was selected as the primary result for a more conservative retrospective evaluation. Neither model has been validated for predicting future customer cancellations.

## Business Recommendations

1. Evaluate targeted retention incentives for month-to-month customers.

2. Investigate service quality and support experiences among fiber optic customers.

3. Review billing experiences associated with electronic check payments.

4. Explore early engagement strategies for newer customers with higher monthly charges.

## Limitations

The dataset does not contain direct measures of customer satisfaction, complaints, or service quality. Therefore, observed relationships should not be interpreted as confirmed causes of churn.

Model evaluation is retrospective and does not establish future predictive performance.

## Conclusion

This project demonstrates how customer analytics and machine learning can help identify high-risk customer segments, evaluate predictive patterns, and translate analytical findings into practical retention recommendations.
