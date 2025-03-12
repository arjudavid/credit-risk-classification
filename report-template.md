# Module 12 Report Template

## Overview of the Analysis

### Purpose of the Analysis
The purpose of this analysis is to develop a machine learning model that can predict loan risk—whether an applicant is a low-risk (0) or high-risk (1) borrower.

### Dataset 
The dataset contains financial information about loan applicants, including credit history, loan amount, and income levels. The primary goal is to predict whether an applicant is a high-risk borrower.

### Target Variable & Feature Selection
* Target Variable (y): Loan risk classification (0 = low risk, 1 = high risk)
* Features (X): Various financial factors that influence loan risk (incomes, loan amount, number of accounts, etc).

### Stages of Machine Learning Process
1. Data Preprocessing: We loaded the dataset and separated it into features (X) and target labels (y).Then we splited the dataset into training and testing sets using train_test_split().

2. Model Selection & Training: Used the Logistic Regression from scikit-learn to classify loan applicants. Fitted the model using X_train and y_train, and then we
generated predictions (y_pred) on the test dataset.

3. Model Evaluation: We Created a confusion matrix to analyze correct and incorrect predictions, and then measured accuracy, precision, recall, and F1-score to evaluate model performance.

## Results
*Accuracy (99%): The model correctly classified 99% of all loan applicants, making it highly reliable in predicting loan risk.

*Precision: For low-risk applicants, precision is 100%, meaning all predicted low-risk borrowers were correctly classified. For high-risk applicants, precision is 84%, indicating that 16% of flagged high-risk applicants were actually low-risk.

*Recall: The recall for low-risk applicants is 99%, confirming that nearly all actual low-risk borrowers were correctly identified. The recall for high-risk applicants is 94%, meaning the model effectively captures the majority of true high-risk borrowers.

#### Performance Metrics:
- Accuracy: 99%
- Precision:
      Low-risk (0): 1.00 (100%)
      High-risk (1): 0.84 (84%)
- Recall:
      Low-risk (0): 0.99 (99%)
      High-risk (1): 0.94 (94%)

## Summary

* Which one seems to perform best? How do you know it performs best? Since we only used Logistic Regression, this model was the best-performing. It achieved an accuracy of 99%, indicating very high predictive performance.
  
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? ) Yes. While the model has a high accuracy score, it is crucial to focus on recall for high-risk borrowers (1s).

* For example: High recall (94%) for high-risk loans means that the model correctly identifies most risky borrowers, which is critical for a bank to minimize defaults. However, precision for high-risk loans is 84%, meaning that 16% of flagged high-risk borrowers might actually be low-risk, which could result in rejecting good applicants.

**Final Recommendation!** This Logistic Regression model is highly effective at predicting loan risk and should be used by financial institutions. However, further refinements could be made, like; fine-tuning the threshold to optimize precision vs. recall, Using alternative models  for comparison. But, overall this model provides an excellent starting point for risk prediction. 
