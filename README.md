# Introduction

This project aims to apply machine learning techniques to solve a credit risk problem using the credit card credit dataset from LendingClub. The primary objective is to handle class imbalance by applying oversampling and undersampling techniques and evaluating different machine learning models for credit risk prediction.

To achieve this, we utilize the imbalanced-learn and sci-kit-learn libraries to build and evaluate models using resampling techniques. The key models used in this analysis include BalancedRandomForestClassifier and EasyEnsembleClassifier. The project also provides a written recommendation on the most effective model for predicting credit risk.

# Methodology

## Steps:

Initial Model Evaluation: Evaluated three machine learning models using resampling techniques to determine which performs best in predicting credit risk.

Oversampling Techniques: Applied methods such as RandomOverSampler and SMOTE to balance the dataset.

Undersampling Technique: Used ClusterCentroids to reduce the majority class size.

Logistic Regression Classifier: Trained a logistic regression model to compute the balanced accuracy score, generate a confusion matrix, and evaluate classification performance.

SMOTEENN Resampling: Implemented a combinatorial approach of over- and undersampling using SMOTEENN to assess its effectiveness compared to previous resampling techniques.

Ensemble Models: Trained and compared two ensemble classifiers (BalancedRandomForestClassifier and EasyEnsembleClassifier) using resampling techniques.

Final Evaluation: Calculated the balanced accuracy score, generated confusion matrices, and created classification reports to assess model performance.

# Overview of the Analysis

X (Independent Variable): Features used to train the models.

y (Dependent Variable): The target variable, where loan status is categorized as either low-risk or high-risk.

Training Process: The data was split into x-train and y-train to train the models, then tested using X-test. Finally, y-test and y-pred were used to fit the final models and compare predictions with actual results.

Target Definition: Loan-status was set as the target, and all data classified as high risk were grouped together.

# Results

### Resampling Models for Credit Risk Prediction

Naive Random Oversampling

Balanced Accuracy Score: 79.43%

High Risk Precision: 1%

High Risk Recall: 75%

F1 Score: 2%

Downside: Can lead to overfitting.

### SMOTE (Synthetic Minority Oversampling Technique)

Balanced Accuracy Score: 78.61%

High Risk Precision: 1%

High Risk Recall: 63%

F1 Score: 2%

Downside: Takes longer to process compared to random oversampling.

### Cluster Centroids (Undersampling)

Balanced Accuracy Score: 66.83%

High Risk Precision: 1%

High Risk Recall: 69%

F1 Score: 1%

Downside: May remove important data, leading to a loss of information.

### SMOTEENN (Combination of Oversampling & Undersampling)

Balanced Accuracy Score: 64.49%

High Risk Precision: 1%

High Risk Recall: 72%

F1 Score: 2%

Downside: The longest processing time but yielded the most accurate results among resampling models.

### Ensemble Classifiers for Credit Risk Prediction

Balanced Random Forest Classifier

Balanced Accuracy Score: 78.85%

High Risk Precision: 3%

High Risk Recall: 70%

F1 Score: 6%

Most Important Feature: "Next Payment" with an importance score of 0.021538.

### Easy Ensemble AdaBoost Classifier

Balanced Accuracy Score: 92.01%

High Risk Precision: 9%

High Risk Recall: 89%

F1 Score: 17%

Downside: Longer processing time but highest accuracy.

# Conclusion

### Among all models evaluated, the Easy Ensemble Classifier demonstrated the best performance with:

92.01% balanced accuracy

9% precision for high-risk loans

89% recall for high-risk loans

Highest F1 Score (17%)

### This suggests that the Easy Ensemble Classifier is the most effective model for credit risk prediction in this dataset, significantly outperforming other resampling techniques and classification models.

Model Performance Ranking (Descending Order for High-Risk Prediction):

Easy Ensemble Classifier - 92.01% accuracy, 9% precision, 89% recall, 17% F1 Score

Balanced Random Forest Classifier - 78.85% accuracy, 3% precision, 70% recall, 6% F1 Score

SMOTE Oversampling - 78.61% accuracy, 1% precision, 63% recall, 2% F1 Score

Naive Random Oversampling - 79.43% accuracy, 1% precision, 75% recall, 2% F1 Score

SMOTEENN - 64.49% accuracy, 1% precision, 72% recall, 2% F1 Score

Cluster Centroids - 66.83% accuracy, 1% precision, 69% recall, 1% F1 Score

### This analysis highlights the importance of handling imbalanced datasets and demonstrates that ensemble models, particularly the Easy Ensemble Classifier, can significantly improve credit risk predictions.

