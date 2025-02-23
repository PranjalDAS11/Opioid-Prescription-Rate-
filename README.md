# Opioid Prescription Rate Analysis
Predicting and Analyzing Over-Prescription of Opioids Using Medicare Part D Data

## Problem Statement
The opioid crisis remains one of the most pressing public health issues, with over 130 people dying every day due to opioid overdoses. Prescription opioids contribute significantly to this crisis, with 46 deaths daily linked to prescription opioids. Traditional approaches focus on treating addiction or identifying at-risk patients, but these methods involve significant social and economic costs and may induce moral hazard.

#Why This Project?
Instead of solely addressing patient-side risks, our approach shifts the focus to identifying opioid over-prescribers—healthcare providers whose prescription rates far exceed national or regional averages. By leveraging large-scale Medicare Part D data, we aim to build predictive models that classify prescribers as potential over-prescribers based on various state policies, socio-economic factors, and prescribing behaviors.

## Dataset
We utilized the Medicare Part D Prescribers dataset from CMS Open Data, which includes over 25 million records. Key attributes include:

Prescriber State & Specialty
Opioid Prescription Rate per 100 People
State-Level Policy Factors
County-Level Socio-Economic Indicators

Dataset Link - https://data.cms.gov/provider-summary-by-type-of-service/medicare-part-d-prescribers/medicare-part-d-prescribers-by-provider-and-drug/data

## Methodology
1. Exploratory Data Analysis (EDA)
Extracted opioid prescription rate and grouped data by prescriber state and specialty.
Integrated state policy and county-level factors such as median income, education, and unemployment rates.
Visualized prescription trends using heatmaps and pie charts.
2. Predictive Modeling
We developed three classification models to predict opioid over-prescribers:

Logistic Regression
Random Forest
XGBoost (Best Model - 89% Accuracy)
To address class imbalance, we applied SMOTE and feature selection techniques.

3. Model Interpretability
Using SHAP (SHapley Additive Explanations) analysis, we identified key drivers of over-prescription. The most influential feature was the opioid prescription rate, which accounted for nearly 50% of the model’s predictive power.

#Key Findings
States with strict opioid regulations had significantly lower prescription rates.
Counties with higher median income and education levels exhibited lower opioid prescription rates.
Providers specializing in pain management and internal medicine had the highest likelihood of over-prescription.
XGBoost outperformed other models, achieving 89% accuracy in detecting over-prescribers.
Impact & Future Work
By identifying high-risk prescribers, this project provides data-driven insights to optimize opioid prescription patterns. This can aid policymakers and healthcare regulators in implementing targeted interventions, ultimately reducing opioid misuse.

## Future research could explore:

Spatio-temporal analysis of prescription trends.
Impact of pharmaceutical sales and marketing on prescription rates.
Integration with real-time electronic health record (EHR) data for better tracking.
