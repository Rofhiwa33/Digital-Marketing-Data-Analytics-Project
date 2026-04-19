# Improving success in telemarketing: An application of statistical methods in the banking industry 

## Overview

This project applies statistical learning techniques to improve telemarketing effectiveness in the banking sector.

Using a real-world dataset of 45,211 customer records, the study builds predictive models to identify customers who are most likely to subscribe to long-term deposit products.

The goal is to help banks:

* Improve targeting strategies
* Reduce unnecessary customer contact
* Increase conversion rates


## Research Objective

To evaluate whether Logistic Regression and Decision Tree models can accurately predict customer response to telemarketing campaigns in a South African bank.

📂 Dataset
* Source: Bank telemarketing dataset
* Observations: 45,211
* Features: 20 variables (reduced to 19 after cleaning)
* Target Variable: deposit_take_up (Yes/No)
  
## Key Variables:
* Customer demographics (age, marital status, occupation)
* Financial information (balance, loans)
* Campaign details (contact time, previous campaigns)

Methodology
###### 1. Data Preparation
* Removed duplicates (6 records)
* Corrected unrealistic values (e.g., age 0–150 → 18–100)
* Handled outliers using:
* Winsorization (1st–99th percentile)
* Robust scaling
* Addressed class imbalance using SMOTE
* Feature encoding (One-hot & ordinal encoding)

###### 2. Exploratory Data Analysis (EDA)
* Distribution analysis (histograms)
* Categorical comparisons (bar charts, stacked plots)
* Correlation analysis (Pearson heatmap)

## Key observations:

* Most customers do not accept deposits
* Highest engagement in May
* Contact time and previous campaigns show strong influence

3. Model Development
###### Logistic Regression
Accuracy: 79%
ROC AUC: 0.89
Strong interpretability

Insight:

Performs well for non-depositors
Struggles with precision for depositors

###### Decision Tree
Accuracy: 90% (after cross-validation)
ROC AUC: 0.86

Insight:

Initially overfitted → fixed using 5-fold cross-validation
Better overall predictive performance than logistic regression


## Key Findings
* Contact time is one of the strongest predictors
* Previous campaign success significantly increases conversion likelihood
* Most customers decline offers → class imbalance is a major challenge
* Both models perform better at predicting non-depositors than depositors
  
## Business Recommendations
* Target customers with previous positive campaign responses
* Optimize contact timing to improve success rates
* Continuously update models with new data
* Balance model accuracy with interpretability (use Decision Trees + SHAP if needed)
* Ensure compliance with POPIA (data privacy regulations)

## What I Learned
* Building end-to-end predictive models
* Handling real-world data issues (outliers, imbalance, anomalies)
* Applying classification techniques in business problems
* Improving model performance using cross-validation
* Translating analysis into business insights
  
📁 Project Structure
Digital-Marketing-Data-Analytics-Project/
│── data/                # Raw and cleaned dataset

│── notebooks/           # Jupyter notebooks (EDA & modelling)

│── outputs/             # Visualizations and results

│── report/              # Research report

## Tools & Technologies
* Python (Pandas, NumPy, Scikit-learn)
* Matplotlib & Seaborn (Visualization)
* Jupyter Notebook
* SMOTE (Imbalanced data handling)
