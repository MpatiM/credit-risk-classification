# Credit Risk Classification
The Module 20 assignment was completed to asses understanding of Machine Learning Supervised Learning.

**Following subsections were performed:**
* Split the Data into Training and Testing Sets
* Create a Logistic Regression Model with the Original Data
* Write a Credit Risk Analysis Report

## Split the Data into Training and Testing Sets
Open the starter code notebook and use it to complete the following steps:
1.	Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.
2.	Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.

>_**NOTE:**_ A value of '0' in the “loan_status” column means that the loan is healthy. A value of '1' means that the loan has a high risk of defaulting.

3.	Split the data into training and testing datasets by using train_test_split.

## Create a Logistic Regression Model with the Original Data
Use your knowledge of logistic regression to complete the following steps:
1.	Fit a logistic regression model by using the training data (X_train and y_train).
2.	Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.
3.	Evaluate the model’s performance by doing the following:
    * Generate a confusion matrix.
    * Print the classification report.
4.	Answer the following question: **How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?**

## Credit Risk Analysis Report
The purpose of fitting the Logistic Regression Model to the lending data is to classify and test the prediction accuracy of whether the data is considered a healthy loan, marked '0', or a high-risk loan, marked as '1'. Once we can assess the classification, if the prediction rate is good, that means the model can be used reliably to classify lending data loan status.

Model Scores:
* Accuracy Score: 0.99 -> 99% accuracy
* Precision Score:
    * Healthy loan - 1.00 -> 100% precision
    * High-Risk loan - 0.85 -> 85% precision
* Recall Score:
    * Healthy loan - 0.99 -> 99% recall
    * High-Risk loan - 0.91 -> 91% recall

The logistic regression model does really well overall with an accuracy of 99%. The model does the best in predicting '0', healthy loan, where the precision is 100% and recall is 99%. The model also predicts '1', high-risk loan, just as well with a precision of 85% and a recall of 91% but the overall percentage of prediction is lower. However, the model can be improved since the balance between healthy loan and high-risk loan is not balanced. About 96% (18765 out of 19384)of the data is considered a healthy loan and accurately predicts 18663 points of data. On the other hand, only 619 out of 19384 of the data is considered high-risk loan and accurately predicts 563 points of data. If the model were to balance the data between the two to become more even, the model prediction may change but it would make the resulting accuracy more reliable, so therefore, I would recommend this model.
