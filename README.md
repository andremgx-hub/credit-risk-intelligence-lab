
# Credit Risk Intelligence Lab
Credit Risk Intelligence Lab is a machine learning project focused on credit risk analysis. The objective is to estimate probability of default, discover hidden borrower segments through unsupervised learning, detect anomalous credit profiles, and generate interpretable portfolio-level risk insights.

## Project Motivation
Credit risk is not only a classification problem. A borrower can be classified as high or low risk, but financial institutions also need to understand why that risk exists, whether similar borrowers form hidden groups, and which profiles may require additional review.

This project combines supervised learning, unsupervised learning, anomaly detection, explainability, and risk metrics to build a more complete credit risk analysis framework.

## Main Questions
1. Which borrowers have the highest probability of default?
2. What hidden borrower segments exist within the credit portfolio?
3. Which borrowers look anomalous compared with the rest of the portfolio?
4. Which variables explain the estimated credit risk?
5. How can risk be summarized at portfolio and segment level?

## Planned Methodology
The project will be developed in stages:

- Exploratory data analysis
- Feature engineering
- Probability of default modeling
- Unsupervised borrower segmentation
- Anomaly detection
- Model explainability
- Portfolio-level risk reporting
- Streamlit dashboard

## Repository Structure

```text
credit-risk-intelligence-lab/
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── README.md
│
├── notebooks/
│
├── src/
│   └── credit_risk_lab/
│       ├── __init__.py
│
├── reports/
│   ├── figures/
│   └── credit_risk_report.md
│
├── app/
│   └── streamlit_app.py
│
├── tests/
│
├── .gitignore
├── LICENSE
├── README.md
├── requirements.txt
└── pyproject.toml