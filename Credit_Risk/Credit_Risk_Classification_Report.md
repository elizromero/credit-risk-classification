
# Module 12 Report: Credit Risk Classification

## Overview of the Analysis

The objective of this analysis was to use a logistic regression model to classify loans as either `0` (healthy loan) or `1` (high-risk loan). The dataset contained various financial variables such as loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. The target variable, `loan_status`, indicates the risk status of each loan.

The machine learning process involved the following stages:
1. Data preparation, including separating features (`X`) and labels (`y`), and splitting the data into training and testing datasets.
2. Training a logistic regression model on the training data.
3. Evaluating the model's performance on the testing data using metrics such as confusion matrix, accuracy, precision, recall, and F1-score.

The analysis specifically used the `LogisticRegression` class from scikit-learn, with a maximum iteration limit of 200 and random state set to 1 for reproducibility.

---

## Results

* **Logistic Regression Model**:
  - **Accuracy**: 99%
  - **Precision**:
    - For `0` (healthy loans): 100%
    - For `1` (high-risk loans): 85%
  - **Recall**:
    - For `0` (healthy loans): 99%
    - For `1` (high-risk loans): 91%
  - **F1-Score**:
    - For `0` (healthy loans): 100%
    - For `1` (high-risk loans): 88%

The confusion matrix provided the following insights:
- **True Negatives (Healthy loans correctly identified)**: 18,663
- **False Positives (Healthy loans incorrectly classified as high-risk)**: 102
- **False Negatives (High-risk loans incorrectly classified as healthy)**: 56
- **True Positives (High-risk loans correctly identified)**: 563

---

## Summary

The logistic regression model demonstrates excellent overall performance in classifying both healthy and high-risk loans, achieving an accuracy of 99%. It performs exceptionally well at predicting healthy loans, with perfect precision and F1-score and a recall of 99%. For high-risk loans, the model shows strong results with a precision of 85%, recall of 91%, and F1-score of 88%, indicating it is effective at identifying loans at risk.

### Recommendation:
This model is highly reliable for identifying both loan categories, but if minimizing false positives or false negatives for high-risk loans is crucial (e.g., avoiding risky loans), further fine-tuning or alternative models could be explored to improve the precision for high-risk loans without compromising recall.
