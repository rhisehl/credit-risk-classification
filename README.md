# Credit Risk Classification Report

## Overview of the Analysis
The purpose of the analysis is to determine if a supervised learning model could accurately and precisely predict the risk level of an individual loan. The data was a set of lending data including the loan amount and interest rate, as well as the borrower's income, debt:income, number of accounts, number of derogatory marks, and total debt amount. 

The dataset contained 75036 healthy loans and 2500 high-risk loans.

The data was first run through a LogisticRegression model in its raw form. Then, the data was resampled using RandomOverSampler and rerun through the LogisticRegression model.


## Results

* Machine Learning Model 1:
  * Balanced accuracy score: 95.2%
  * Precision: 100% for healthy loans, 85% for high-risk loans (
    *Reminder: Of all predicted healthy loans, 100% were healthy. Of all predicted high-risk loans, 85% were actually high-risk
  * Recall: 99% for healthy loans, 91% for high-risk loans
    *Reminder: Of all healthy loans, the model predicted 99% correctly. Of all high-risk loans, the model predicted 91% correctly
   
* Machine Learning Model 2:
  * Balanced accuracy score: 99.4%
  * Precision: 100% for healthy loans, 84% for high-risk loans
    *Reminder: Of all predicted healthy loans, 100% were healthy. Of all predicted high-risk loans, 84% were actually high-risk
  * Recall: 99% for healthy loans, 99% for high-risk loans
    *Reminder: Of all healthy loans, the model predicted 99% correctly. Of all high-risk loans, the model predicted 99% correctly


## Summary

The machine learning models, overall, were fairly accurate in predicting loan risks. The first model would be sufficient if the goal were to predict healthy loans, as its predictions in this department were nearly perfect. It would not, however, be the best bet for high-risk predictions. This is because only 85% of its predicted high-risk loans were actually high-risk.

The second model performed 1% worse for high-risk precision, but performed 8% better with high-risk recall. This means it is almost perfectly accurate at finding all of the actual high-riks loans, but about 16% of the time, the loans it lists as high-risk were not high-risk.

Overall, the second model is likely the better option in all cases. While the second model loses 1% precision on high-risk loans, that is balanced out by the increased recall. This is also shown in the f1 score for high-risk loans (.91 for case 2, .88 for case 1). 
