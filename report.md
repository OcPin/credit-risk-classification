# Module 12 Report

## Overview of the Analysis

The primary objective of this analysis was to develop machine learning models to predict loan risk based on financial data. 

The dataset contains financial attributes related to loan applicants, including loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. 

The goal is to use this information to predict and classify loans into two categories: Healthy Loans (Class 0) and High-Risk Loans (Class 1) based on their associated risk factors or repayment potential. 

The analysis began by collecting lending data from a CSV file, followed by dividing it into features and the target variable ('loan_status'). The data was split into training and testing sets for model training and evaluation. 

In the analysis, the scikit-learn library's LogisticRegression method was used for its suitability in binary classification tasks and was trained using the training dataset. Subsequently, predictions were made on the test data, and various metrics were computed to assess the model's performance. Additionally, the imbalanced-learn library's RandomOverSampler was implemented to tackle class imbalance. This technique addresses skewed class distributions, specifically in the context of high-risk loans, by generating synthetic samples to create a more balanced dataset for improved model training and performance in predicting high-risk loans accurately.

## Results

* Machine Learning Model 1:
  * Balanced Accuracy Score: 0.952
  * Precision (Class 0 - Healthy Loan): 1.00
  * Recall (Class 0 - Healthy Loan): 0.99
  * Precision (Class 1 - High-Risk Loan): 0.85
  * Recall (Class 1 - High-Risk Loan): 0.91



* Machine Learning Model 2:
  * Balanced Accuracy Score: 0.994
  * Precision (Class 0 - Healthy Loan): 1.00
  * Recall (Class 0 - Healthy Loan): 0.99
  * Precision (Class 1 - High-Risk Loan): 0.84
  * Recall (Class 1 - High-Risk Loan): 0.99

## Summary

Model 1 excels in identifying healthy loans, demonstrating a commendable balance between precision and recall. While it exhibits a slightly lower precision for high-risk loans, it still maintains robust recall. The balanced accuracy score underscores its overall strong predictive performance across both classes.

On the other hand, Model 2 showcases outstanding proficiency in identifying both healthy and high-risk loans. Similar to Model 1, it maintains high precision and recall for healthy loans. For high-risk loans, it exhibits a marginal decrease in precision but retains exceptional recall. The elevated balanced accuracy score signals superior overall predictive capability compared to Model 1.

Considering the critical task of correctly identifying high-risk loans while minimizing false alarms, Model 1 may be a preferred choice due to its higher precision (0.85) for high-risk loans (Class 1) compared to Model 2's precision (0.84) for the same class.

Although Model 2 boasts a slightly higher recall for Class 1, the elevated precision of Model 1 implies a potential reduction in false alarms, a crucial aspect in financial contexts to avoid unwarranted risk assessments or actions on healthy loans.