# credit-risk-classification

## Overview

This project focuses on predicting the risk of loans using machine learning, specifically through a Logistic Regression model. The goal is to classify loans as either "healthy" (low-risk) or "high-risk" based on financial data such as credit history, income, loan amount, and other features. The results from this analysis help financial institutions mitigate risks by identifying potential high-risk loans early.

## Purpose of the Analysis

The main purpose of this analysis was to develop and evaluate machine learning models to predict loan risk. Using a dataset that includes various financial details, the model helps classify whether a loan falls into the category of:
- **0**: Healthy (low-risk)
- **1**: High-risk

- ## Machine Learning Process

The machine learning pipeline involved several steps:
1. **Data Preparation**: Preprocessing steps like handling missing values, normalizing numerical features, and encoding categorical variables.
2. **Data Splitting**: Dividing the dataset into training and testing sets to validate the model's performance.
3. **Model Selection**: A Logistic Regression model was used due to its simplicity and effectiveness in binary classification tasks.
4. **Model Evaluation**: Metrics such as accuracy, precision, recall, and F1-score were calculated to assess model performance, with a focus on precision and recall for high-risk loans due to the class imbalance.

## Results

### Logistic Regression Model

The Logistic Regression model was evaluated on the testing dataset. The results for both healthy and high-risk loans are summarized below:

- **Accuracy**: 99%
- **Precision for healthy loans (0)**: 1.00
- **Recall for healthy loans (0)**: 0.99
- **F1-score for healthy loans (0)**: 1.00
- **Precision for high-risk loans (1)**: 0.85
- **Recall for high-risk loans (1)**: 0.95
- **F1-score for high-risk loans (1)**: 0.89
- **Macro average F1-score**: 0.94

## Summary of Findings

The Logistic Regression model performs exceptionally well, with an accuracy of 99%. The model accurately classifies healthy loans and effectively identifies high-risk loans, which is critical for risk management in financial applications. 

- **Recommendation**: Based on the high recall for high-risk loans (1’s), the Logistic Regression model is recommended for scenarios where identifying high-risk loans is of greater importance. Minimizing false negatives (i.e., failing to identify a high-risk loan) is crucial in financial institutions, and this model's performance on high-risk loans makes it suitable for this use case.