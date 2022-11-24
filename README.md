# Logistical_Regression

Using logistical regression to create a model to predict risky loans.

    Split the Data into Training and Testing Sets
    Create a Logistic Regression Model with the Original Data
    Predict a Logistic Regression Model with Resampled Training Data


Split the Data into Training and Testing Sets
Open the starter code notebook and then use it to complete the following steps.

Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.

Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.

Note A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.

Check the balance of the labels variable (y) by using the value_counts function.

Split the data into training and testing datasets by using train_test_split.

Create a Logistic Regression Model with the Original Data
Employ your knowledge of logistic regression to complete the following steps:

Fit a logistic regression model by using the training data (X_train and y_train).

Save the predictions on the testing data labels by using the testing feature data (X_test) and the fitted model.

Evaluate the model’s performance by doing the following:

Calculate the accuracy score of the model.

Generate a confusion matrix.

Print the classification report.

Answer the following question: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

Predict a Logistic Regression Model with Resampled Training Data
Did you notice the small number of high-risk loan labels? Perhaps, a model that uses resampled data will perform better. You’ll thus resample the training data and then reevaluate the model. Specifically, you’ll use RandomOverSampler.

To do so, complete the following steps:

Use the RandomOverSampler module from the imbalanced-learn library to resample the data. Be sure to confirm that the labels have an equal number of data points.

Use the LogisticRegression classifier and the resampled data to fit the model and make predictions.

Evaluate the model’s performance by doing the following:

Calculate the accuracy score of the model.

Generate a confusion matrix.

Print the classification report.

Answer the following question: How well does the logistic regression model, fit with oversampled data, predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

## Using Logistical Regression Model with Original Data 
                precision    recall  f1-score   support
        0           1.00      0.99      1.00     18765           
        1           0.85      0.91      0.88       619    
        accuracy                        0.99     19384   
        macro avg   0.92      0.95      0.94     19384
        weighted avg0.99      0.99      0.99     19384

## Using Logistical Regression Model with RandomOverSampler 
                precision    recall  f1-score   support
        0           1.00      0.99      1.00     18765           
        1           0.84      0.99      0.91       619   
        accuracy                        0.99     19384   
        macro avg   0.92      0.99      0.95     19384
        weighted avg0.99      0.99      0.99     19384
     
