# Credit Risk Classification  
**Creator**: Luke Roberts  
**Date**: May 2025

## Table of Contents
- [Credit Risk Classification](#credit-risk-classification)
  - [Table of Contents](#table-of-contents)
  - [Project Description](#project-description)
  - [Research Questions to Answer](#research-questions-to-answer)
  - [Features](#features)
  - [Key Findings](#key-findings)
  - [Recommendation](#recommendation)
  - [Methodology](#methodology)
  - [Ethical Considerations](#ethical-considerations)
  - [Opportunities for Further Analysis](#opportunities-for-further-analysis)
  - [Resources](#resources)

## Project Description
This project analyzes financial data from loan applicants to build a machine learning model that classifies credit risk. Using structured lending data, the goal is to determine whether a loan applicant is **high risk** or **low risk**, enabling financial institutions to make more informed lending decisions and reduce the chance of defaults.

## Research Questions to Answer
1. Can machine learning accurately predict whether a loan applicant is likely to default?
2. Which financial variables are most useful in predicting credit risk?
3. How well does a Logistic Regression model perform at identifying high-risk loans?

## Features
- **Binary Classification**: Predicts whether a loan is high risk (`1`) or low risk (`0`).
- **Scikit-learn Model**: Uses Logistic Regression to train and evaluate the model.
- **Performance Metrics**: Includes precision, recall, and f1-score for both risk classes.

## Key Findings
- The dataset was highly imbalanced, with **75,036 low-risk** and **2,500 high-risk** loans.
- The Logistic Regression model achieved:
  - **Accuracy**: 99.18%
  - **Recall (High Risk)**: 90.95%
  - **Precision (High Risk)**: 84.66%
- These metrics show that the model performs very well, especially in identifying high-risk loans, which are the most critical to flag in a financial setting.

## Recommendation
We recommend using the Logistic Regression model for credit risk prediction due to its high accuracy and strong recall on the minority class (high-risk loans). Since financial institutions are more concerned about mistakenly approving risky borrowers, recall for class `1` is crucial — and this model handles that well. For further improvement, additional models like Random Forest or Neural Networks could be evaluated, especially if class imbalance techniques are introduced.

## Methodology
- **Data Source**: `lending_data.csv`
- **Preprocessing**: Split into features and target (`loan_status`)
- **Train-Test Split**: 75% training, 25% testing
- **Model Used**: `LogisticRegression` from `sklearn.linear_model`
- **Evaluation**: Accuracy, confusion matrix, classification report

## Ethical Considerations
All data used was hypothetical and anonymized, ensuring no personally identifiable information was handled. Predictive models should be deployed with caution, as biased input data can lead to unfair loan denial outcomes. Future models should include fairness checks and be validated against discrimination metrics.

## Opportunities for Further Analysis
- Compare multiple classification algorithms (e.g., Decision Trees, Neural Networks)
- Address class imbalance using oversampling (SMOTE) or class weighting
- Analyze feature importance to identify key financial indicators of loan risk
- Build a web app or dashboard for loan officers to interact with predictions

## Resources
- **DU Bootcamp Modules**: Supervised learning & model evaluation
- **ChatGPT**: Assisted with explanation and code validation
