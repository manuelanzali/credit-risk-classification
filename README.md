# credit-risk-classification
Module 20 Challenge

Credit Risk Analysis Report:

The purpose of the analysis was to use techniques to train and evaluate a logistic regression model based on a borrower's loan risk. By using a dataset containing historical lending activity, we built a model to identify the creditworthiness of a borrower.

The financial information this data was on was from a peer-to-peer lending services company and contained loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks, total debt, and loan status. We needed to predict whether providing a loan to certain borrowers would be a high-risk or healthy loan; ie credit risk of a borrower.

The variable we were trying to predict was the loan status based on the other variables (loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks, total debt) in the data.

The stages of the machine learning process we went through to analyze the original data were we first used train_test_split to split the data into training and testing datasets, after splitting the x and y data and creating labels. We then used the training data to fit a logistic regression model by using a classifier. Next, we made predictions based on the testing data and the model that was just fitted. This helped us to then evaluate how well the Logistic Regression model made predictions by using the confusion matrix and classification report. The classification report helped us to analyze the precision, recall, f1-score, support, and accuracy of our Logistic Regression model in predicting both high-risk (high credit risk) and healthy (low credit risk) loans.


## Results

            precision    recall  f1-score   support

            0       1.00      1.00      1.00     18759
            1       0.87      0.95      0.91       625

    accuracy                           0.99     19384
   macro avg       0.94      0.97      0.95     19384
weighted avg       0.99      0.99      0.99     19384

. Accuracy Scores: This score helped us to see the overall validity of the model's predictions; correct predictions/total predictions. In this credit risk analysis, we can see that out of all of the predictions made, the model was 99% correct in all predictions of credit risk.

. Precision: This score helps us see the ratio of how accurate the positive predictions that were made are in each class; the Predicted Positive/Total Predicted Positive Predictions. In this analysis, we find that there is a higher precision of the model in predicting label 0/low credit risk versus label 1/high credit risk.

. Recall Scores: This score helps us see the ratio of predicted positive/all predicted in each class. In this analysis, we can inferthat there is a higher recall for the model predicting label 0 over label 1 which shows us that there is a high comprehensive output and low false negative output for label 0/low credit risk borrowers.



## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best? (ie. Which model would I like to try based off of the prediction scores from the logistic regression model? Give a few sentences on why based on what was taught and learned from class)

The Logistic Regression Model works really well as shown by the accuracy score. The machine learning model that seems to work the best and that I would like to try would be the Random Forest Algorithm Model as this model would allow us to use several trees as weak leanrers beased on a few columns of the data each, and together would work to be a strong predictor; ensemble learning. Also, if we create a custom loss function that shows what we are wanting to get out of the model vs what the model actually provides us with or use feature engineering to create each feature ourselves to make sure everything we need is accounted for this may be additionally helpful. 

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? ) 

The performance does depend on the problem we are trying to solve because of context; if the model is better at predicting the high risk loan borrowers/1's, this will help companies to root out the highest risk borrowers using the model. The performance would be based on the problem we are trying to solve and the characteristics of the data. For example, if a company's goal were to be to help high risk borrowers, they would need to change some characteristics to ensure the model is better at predicting the 1's in the data, rather than a balance in accuracy of the model in predicting both 1's and 0's.
