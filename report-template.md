# Module 12 Report Template

## Overview of the Analysis

The purpose of this analysis is to predict loans which have a higher probility of being bad loans and have a higher probability of default. the objective of the analysis is to model that should be able to predict 100% of the default loans with 100% accuracy.  

# Available Data: 
The available data includes 
a. loan size
b. interest rate
c. Income
d. debt to income ratio
e. number of accounts
f. deregotory remarks
g. total debt 
h. loan status

The loan status is the what we are trying to predict so that we can predict if they should e approved or not. in the original data we found **2500** records which have a status of default where as **75036** (this is imbalanced data) 

The process for the implementation of the LogisticRegression is as following. 
    1. Review data
    2. Separate data between X (Features) and y (predictive) data
    3. using train_test_split to break the data into model
    4. set up a model 
    5. fit the data
    6. predict the results of the model

the LogisticRegression is statistical model where the probability of an event taking place by having the log-odds for the event be a linear combination of one or more independent variables


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
                      precision    recall  f1-score   support
               0       1.00      0.99      1.00     18765           
               1       0.85      0.91      0.88       619
               accuracy                    0.99     19384   
               macroavg 0.92      0.95      0.94     19384
               weightedavg 0.99   0.99      0.99     19384



* Machine Learning Model 2: (OverSampledModel)
  * Description of Model 2 Accuracy, Precision, and Recall scores.
                      precision    recall  f1-score   support          
                0       1.00        0.99      1.00    18765           
                1       0.84      0.99        0.91      619    
            accuracy                          0.99    19384   
            macro avg    0.92      0.99      0.95     19384
            weighted avg 0.99      0.99      0.99     19384



## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* the OverSampled Model is better than standard model because of better recall in predicting defaulting loans which almost the same precision as the first model.  

I would not recommend either of the models and would look for models which would be able to predict 100% of 1 with 100% precision while that model can have a lower predictibility for 0, its better to predict and take action on non-defaulting loans inaccuracy as comparative to defulting loans. 
