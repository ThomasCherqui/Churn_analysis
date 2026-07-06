# Customer Churn Analysis

This repository contains a self-contained churn analysis based on an anonymized customer dataset. The goal is to identify the main drivers of churn, quantify the business impact, and propose concrete retention priorities.

## Contents

- `analysis.ipynb`: main notebook with data cleaning, exploratory analysis, business impact analysis, segmentation, and predictive modeling.
- `dataset_churn.csv`: input dataset used in the analysis.

## Analytical Approach

The analysis follows three steps:

1. **Understand churn dynamics**  
   Explore churn rates across customer demographics, contract type, services, payment method, tenure, and monthly charges.

2. **Quantify business impact**  
   Move beyond churn rate by estimating monthly revenue at risk and identifying the segments that concentrate the largest potential loss.

3. **Prioritize retention actions**  
   Train a simple logistic regression model and use predicted churn probabilities to rank customers by risk, showing how targeted retention can focus on the highest-risk groups.

## Key Findings

- Overall churn is about `26.5%`.
- Churn is highly concentrated among `Month-to-month` customers, `Fiber optic` users, and customers paying by `Electronic check`.
- Customers with low tenure are especially exposed, but tenure and contract type are distinct: tenure measures how long a customer has been with the company, while contract type reflects the commercial commitment.
- The model reaches a ROC-AUC of about `0.84`; the top `10%` highest-risk customers have a churn rate around `76%`, almost 3x the population average.

## Recommended Direction

The most actionable retention priority is early-life churn among customers with flexible contracts and high-risk service/payment profiles. A practical next step would be to test targeted onboarding, payment-method migration, or annual-plan conversion campaigns on these segments.

## Limitations

The dataset is static and observational. It supports prioritization and hypothesis generation, but not causal conclusions. Additional data such as usage, support tickets, acquisition channel, margins, and churn reasons would be needed to design and evaluate interventions more rigorously.

## How to Run

Open `analysis.ipynb` in Jupyter or Colab and run all cells. The notebook loads the local CSV file when available.
