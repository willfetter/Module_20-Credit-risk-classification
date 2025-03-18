# Module 20 Report Template

## Overview of the Analysis

The purpose of this analysis was to use various techniques to train and evaluate a model based on loan risk. It used a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers. 

The starter financial data was located within a "lending_data.csv" file and contained the loan status which was either "0" for a healthy loan or "1" for a high-risk loan. The variables we were trying to predict with the models were how many loans are predicted to be healthy and high-risk, versus how many actually are healthy and high-risk. 

The model is built using the dependent variable "y" is loan status, while the independent variable "x" represents all other data including loan size, interest rate, borrower income, debt to income ratio, number of accounts, derrogotory marks, and total debt. 

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
![Original-Accuracy_Score](https://github.com/user-attachments/assets/a04402fd-4acd-4a76-bb91-fffa5ceda1fb)



#### Confusion Matrix
#### Classification Matrix

### Machine Learning Model #2 (Re-Sampled Data)
#### Balanced Accuracy Score
#### Confusion Matrix
#### Classification Matrix


The target variable "y", was used to represent the loan status, and the variable "x" was used to reppresent all other data. 
 



In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
