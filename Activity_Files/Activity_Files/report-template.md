# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis. 
  * A: The purpose of the analysis is the predict the likelyhood of a barrower defaulting on a loan using machine learning models.
* Explain what financial information the data was on, and what you needed to predict. 
  * A: The CSV contains financial information about individual loan applicants. 
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`). 
  * A: I was trying to ultimately predit whether a barrower would be a high risk loan applicant or not. To sum up, the data is highly imbalanced with far more low risk loans than high risk. It may mean the models favors predicting low risk loan, or the model may require oversampling to avoid predicitng everything as low risk loans. 
* Describe the stages of the machine learning process you went through as part of this analysis.
  * Data Prep-  load and explore the data in a pandas dataframe
  * Train-Test Split- Uses train_test_spilt to divide the dataset into (1) taining data (used to train the model) and (2) testing data (used to evaluate model preformance on unseen data)
  * Model Creation- Built sequential neural network using Keras (Input layer, Hidden Layers and Output Layer)
  * Model Training- Trained model using .fit() and chose a number of epochs to learn from the data
  * Model Evaluation- Evaluated performance using the .evaluate() method on the test data
  * Model Prediction and Validation- Used predict() on samples to generate predicted probabilities
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).
  * A: The only methode used was LogisticRegression that creates a linear model for binary classification (predicting whether a loan is high or low risk)

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1: LogisticRegression
    * Class 0 — Low Risk (Safe Loan)
        Precision: 99.70%

        Recall: 99.46%

        F1-Score: 99.58%

    *Class 1 — High Risk (Risky Loan)
        Precision: 84.66%

        Recall: 90.95%

        F1-Score: 87.69%

    *Overall Accuracy: 99.18%
## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any.

The credit risk classification analysis used a LogisticRegression model, which provided strong results with an overall accuracy of 99.18%. It demonstrated a high recall of 90.95% and a precision of 84.66% for high-risk loans (class 1), meaning it correctly identified the majority of risky borrowers while maintaining good precision. This is especially valuable in a lending context, where predicting high-risk applicants accurately is more important than predicting low-risk ones, due to the financial impact of loan defaults. Given its strong performance and interpretability, Logistic Regression is recommended for this problem. However, if further improvement is needed, especially for rare high-risk cases, additional models and class imbalance techniques could be explored.


