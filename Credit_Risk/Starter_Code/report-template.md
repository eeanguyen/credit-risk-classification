## Overview of the Analysis

### Purpose of the Analysis
The purpose of this analysis was to build and evaluate machine learning models to predict whether a loan is classified as "healthy" (low-risk) or "high-risk." By analyzing the financial data of various loans, we aim to assist financial institutions in identifying potential high-risk loans early in the process, helping them mitigate risks and make more informed decisions.

### Financial Data and Prediction Goal
The dataset contains financial information about loan applications. Each entry in the dataset includes various features about the applicants, such as credit history, income, loan amounts, and other financial metrics. The goal was to predict the **loan risk status**: whether a loan is a "healthy loan" (0) or a "high-risk loan" (1).

### Variables and Prediction Labels
We aimed to predict a binary outcome, where:
- **0** represents a **healthy loan**.
- **1** represents a **high-risk loan**.

A basic analysis of the distribution of these labels using `value_counts` revealed the following:
- **Healthy loans (0)**: 18,765 instances.
- **High-risk loans (1)**: 619 instances.
This indicates a significant class imbalance, with healthy loans being much more frequent than high-risk loans.

### Machine Learning Process
The machine learning process involved the following stages:
1. **Data Preparation**: Preprocessing the dataset, including handling missing values, normalizing numerical features, and encoding categorical variables.
2. **Data Splitting**: Dividing the dataset into training and testing sets to evaluate model performance.
3. **Model Selection**: We started with a **Logistic Regression** model due to its simplicity and interpretability for binary classification problems. This allowed us to understand the baseline performance.
4. **Model Evaluation**: Using evaluation metrics such as accuracy, precision, recall, and F1-score to assess model performance. Given the imbalanced dataset, we paid special attention to precision and recall for the high-risk loan category.

### Methods Used
The primary method used was **Logistic Regression**, a standard classification algorithm that works well for binary classification tasks. Logistic regression models the probability that an instance belongs to a particular class using a sigmoid function.

## Results
* **Logistic Regression Model**:
    * **Accuracy**: 99%
    * **Precision for healthy loans (0)**: 1.00
    * **Recall for healthy loans (0)**: 0.99
    * **F1-score for healthy loans (0)**: 1.00
    * **Precision for high-risk loans (1)**: 0.85
    * **Recall for high-risk loans (1)**: 0.95
    * **F1-score for high-risk loans (1)**: 0.89
    * **Macro average F1-score**: 0.94

## Summary

### Model Performance
The **Logistic Regression model** performs exceptionally well on the dataset, with an accuracy of 99%. For healthy loans (label 0), it achieves nearly perfect precision, recall, and F1-score, indicating that the model rarely misclassifies healthy loans. For high-risk loans (label 1), the model also performs quite well, with high recall (0.95), meaning that it successfully identifies most high-risk loans. However, its precision for high-risk loans is slightly lower (0.85), meaning some healthy loans are being misclassified as high-risk.

### Recommendation
Based on the results, the **Logistic Regression model** is highly effective, especially when the focus is on **recall for high-risk loans**. If the goal is to minimize false negatives (i.e., missing out on identifying high-risk loans), this model is a strong choice. It balances high accuracy, precision, and recall, particularly excelling in identifying high-risk loans, which are typically more important to predict correctly in financial risk management.

In financial contexts, predicting high-risk loans (1’s) is more critical because the consequences of misclassifying a high-risk loan as healthy could lead to significant financial losses. Hence, this model’s high recall for high-risk loans (0.95) makes it a good fit for this task.

If you do not recommend any of the models, please justify your reasoning.
