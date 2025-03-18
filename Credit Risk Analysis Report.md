# Module 20 Report Template

## Overview of the Analysis

The purpose of this analysis was to use various techniques to train and evaluate a model based on loan risk. It used a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers. 

The starter financial data was located within a "lending_data.csv" file and contained the loan status which was either "0" for a healthy loan or "1" for a high-risk loan. The variables we were trying to predict with the models were how many loans are predicted to be healthy and high-risk, versus how many actually are healthy and high-risk. 

The model is built using the dependent variable "y" as loan status, while the independent variable "x" represents all other data including loan size, interest rate, borrower income, debt to income ratio, number of accounts, derrogotory marks, and total debt. 

The steps of the machine learning process included:
#### Split the Data into Training and Testing Sets
1. Read the lending_data.csv data from the Resources folder into a Pandas DataFrame
2. Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns
3. Check the balance of the labels variable (y) by using the value_counts function
4. Split the data into training and testing datasets by using train_test_split

#### Create a Logistic Regression Model with the Original Data
1. Fit a logistic regression model by using the training data (X_train and y_train)
2. Save the predictions on the testing data labels by using the testing feature data (X_test) and the fitted model
3. Evaluate the model’s performance by doing the following:
    * Calculate the accuracy score of the model
    * Generate a confusion matrix
    * Print the classification report
4. Answer the question, "How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?"

The results of the analysis are displayed within the output accuracy score, confusion matrix, and classification report. 

## Analysis Results

### Machine Learning Model #1 (Original Data)
#### Balanced Accuracy Score
0.967989851522121

The balanced accuracy score of 0.97 for the original data suggests that the model is able to accurately classify obervations. 

#### Confusion Matrix
array([[18655,   110],
       [   36,   583]])

The original data shows 18,655 healthy loans predicted and 583 unhealthy loans predicted. False positives predicted = 110 and false negatives predicted = 36.

#### Classification Matrix
              precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.84      0.94      0.89       619

    accuracy                           0.99     19384
   macro avg       0.92      0.97      0.94     19384
weighted avg       0.99      0.99      0.99     19384

The original data shows a high rate of predicting low-risk loans (recall value = 0.99) than high-risk loans (recall value = 0.94). The model  does predicts unhealthy loans with 84% accuracy and predicts healty loan values  with 100% accuracy.

### Machine Learning Model #2 (Re-Sampled Data)
#### Balanced Accuracy Score
0.9935981855334257

The balanced accuracy score of 0.99 for the re-sampled data suggests that the re-sampled model is able to very accurately classify obervations. 

#### Confusion Matrix
array([[18646,   119],
       [    4,   615]])

The re-sampled data shows 18,646 healthy loans predicted and 615 unhealthy loans predicted. False positives predicted = 119 and false negatives predicted = 4.

#### Classification Matrix
              precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.84      0.99      0.91       619

    accuracy                           0.99     19384
   macro avg       0.92      0.99      0.95     19384
weighted avg       0.99      0.99      0.99     19384

The re-sampled data shows a very high rate of predicting both low-risk loans (recall value = 0.99) and high-risk loans (recall value = 0.99). The re-sampled model still predicts unhealthy loans with 84% accuracy and predicts healty loan values  with 100% accuracy.

## Summary
Based on the analysis results of the two learning models, the re-sampled (second) model is best for use. The re-sampled model has improved recall values (94% original vs 99% re-sampled) indicating improved high-risk loan prediction rates as well as a significantly smaller amount of false positives identified (36 original vs 4 re-sampled). This model therefore would be extremly useful in predictions loans that could default, and would be therefule useful and reliable for the bank to avoid such high-risk loans.

