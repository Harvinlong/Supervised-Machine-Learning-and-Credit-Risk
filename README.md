# Supervised-Machine-Learning-and-Credit-Risk
## Introduction of this project:
The project aims to apply machine learning to solve a credit risk problem. Using the credit card credit dataset from LendingClub, the objective is to oversample and undersample data using different algorithms and techniques to train and evaluate models with unbalanced classes. 

The project will use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling. 

The models that will be used to predict credit risk include BalancedRandomForestClassifier and EasyEnsembleClassifier, and the project will evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

## Steps:

1. First of all, I evaluated three machine learning models using resampling techniques to determine which is better at predicting credit risk. 

2. I first used oversampling techniques such as RandomOverSampler and SMOTE, and then use undersampling techniques like ClusterCentroids algorithm. 

3. Then I trained a logistic regression classifier to calculate the balanced accuracy score, and generate a confusion matrix, and classification report. 

4. Next,  I used the SMOTEENN algorithm to determine if the combinatorial approach of over- and undersampling is better than the resampling algorithms that I used previously. 

5. After that, I trained and compared two different ensemble classifiers, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk and evaluate each model using resampling techniques. 

6. Finally, I calculated the balanced accuracy score, generate a confusion matrix, and classification report to evaluate the performance of each model.


## Overview of the analysis：
X is the independent variable in the data, and y is the dependent variable. The first model is obtained by training the data through the x-train and y-train. Then X-test was used to test the model for the first time. Finally, y-test and y-pred were used to fit the data into the final model and compare it with the original data. In the process, I set loan-status as the target and sum all the data that can be defined as High risk into a high-risk.

## Results: 
-Balanced Random Forest Classifier：
 A type of random forest classifier that uses balanced subsampling to create multiple decision trees, which are then combined to make a final prediction. The subsampling helps to balance the class distribution and reduce the impact of imbalanced data. The most important feature is "next payment", which has a  0.021538 importance.

-Easy Ensemble AdaBoost Classifier：
An ensemble method that uses AdaBoost algorithm to create multiple classifiers, and then combines them to make a final prediction. The method uses different subsamples of the original data to create diverse classifiers, which can improve the performance on imbalanced data. the balance accuracy score is 0.8028.

-Naive Random Oversampling：
A method for handling imbalanced data by randomly duplicating minority class examples to balance the class distribution. This oversampling approach is simple but can lead to overfitting. The accuracy balanced score is 0.7943 in this sampling model.


-SMOTE Oversampling：
Synthetic Minority Over-sampling Technique (SMOTE) is an oversampling method that creates synthetic examples of the minority class by interpolating between existing examples. This method aims to balance the class distribution and reduce the impact of imbalanced data while avoiding overfitting. the accuracy score improved is 0.78608, but it took longer time in the process.


-Undersampling：
A method for handling imbalanced data by removing examples from the majority class to balance the class distribution. This approach can lead to loss of important information. This model shows the lowest balance score 0.66832.


-Combination (Over and Under) Sampling：
A method that combines oversampling and undersampling techniques to balance the class distribution by creating synthetic examples of the minority class and removing examples from the majority class. This approach aims to balance the class distribution while reducing the impact of imbalanced data and avoiding overfitting.It took the longest time to process, which performed the most accurate data: 


Summary: Each one of the model has it's strength and weakness,accuracy is not always the best metric to evaluate a model's performance. Other metrics such as precision, recall, F1-score, AUC-ROC and etc. should be considered as well. However based on the result that I got from this module, combination sampling provided the most accurate result.
