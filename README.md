Credit Risk Classification

Overview
This project focuses on predicting loan risk using a dataset of historical lending activity from a peer-to-peer lending services company. The goal is to classify loans as either "healthy" (low-risk) or "high-risk" based on various features. A logistic regression model was trained and evaluated to determine the likelihood of borrowers defaulting on their loans, helping the company assess creditworthiness.

Dataset
The dataset used in this project (lending_data.csv) includes the following features:

loan_status: Target label (0 = healthy loan, 1 = high-risk loan)
Various features that represent borrower information, such as income and debt-to-income ratio, which are used to predict the risk of loan default.
Steps
1. Data Preparation
The dataset was loaded into a Pandas DataFrame.
The target variable (y) was defined as the loan_status column.
The features (X) were defined as all remaining columns.
The data was split into training (75%) and testing (25%) sets using train_test_split.
2. Model Training
A logistic regression model was trained using the training data (X_train and y_train).
The model was then used to predict the loan status for the test data (X_test).
3. Model Evaluation
The model's performance was evaluated using a confusion matrix and classification report.
Confusion Matrix: Used to evaluate the model's true positive, true negative, false positive, and false negative predictions.
Classification Report: Provides precision, recall, F1-score, and support for each class (healthy and high-risk loans).
Results
Model Performance
The model achieved the following performance metrics:

Accuracy: 99%
Precision:
Healthy loans (0): 1.00
High-risk loans (1): 0.85
Recall:
Healthy loans (0): 0.99
High-risk loans (1): 0.91
F1-Score:
Healthy loans (0): 1.00
High-risk loans (1): 0.88
Confusion Matrix
The confusion matrix shows that the model correctly predicted the majority of healthy and high-risk loans, with a few false positives and false negatives for high-risk loans.

Summary
The logistic regression model demonstrates excellent performance in predicting loan risk, especially for healthy loans. The model's precision and recall for high-risk loans, while strong, indicate that some healthy loans are misclassified as high-risk. Nevertheless, the model's overall accuracy of 99% makes it a reliable tool for predicting loan outcomes.

Recommendation
Given the model's strong performance, it can be recommended for use in assessing loan risk. The high accuracy and strong F1-scores across both classes suggest that the model is effective at identifying both healthy and high-risk loans. However, the company may want to further fine-tune the model or explore other machine learning techniques to improve precision for high-risk loans.
