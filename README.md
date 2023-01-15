# Supervised-Machine-Learning-and-Credit-Risk
Overview of the analysis：
X is the independent variable in the data, and y is the dependent variable. The first model is obtained by training the data through the x-train and y-train. Then X-test was used to test the model for the first time. Finally, y-test and y-pred were used to fit the data into the final model and compare it with the original data. In the process, I set loan-status as the target and sum all the data that can be defined as High risk into a high-risk.

Results: 
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
