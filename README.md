# Credit_Card_Fraud_Detection

In this project, we consider an imbalanced dataset of credit card frauds (with the target labels being authentic and fraudulent) and build an anomaly detection system to identify transactions that are, in some sense, different from the usual, authentic transactions. These observations are flagged as potentially fraudulent and put to further verification.

We carry out necessary feature extraction and feature transformation.
As the anomaly detection algorithm suffers from high-dimensional data, we figure out the most relevant features separating the target classes, and use only those in the modeling purpose.
Based on the training data, we fit a multivariate normal distribution.
Given a new transaction, if the corresponding density value of the fitted distribution is lower than a pre-specified threshold, then we flag the transaction as fraudulent.
In this notebook, we focus more on the true positive class (the class of fraudulent transactions) than the true negative class (the class of authentic transactions). This is because a false negative (the algorithm predicts a fraudulent transaction as authentic) is far more dangerous than a false positive (the algorithm predicts an authentic transaction as fraudulent, which can always be cross-verified). For this reason, we use F2_score as the evaluation metric.
The choice of the threshold is optimised by iterating over a pre-specified set of values, predicting on the validation set, and evaluating the predictions by means of the  
F2_score.

## our dataset: 
Credit Card Fraud Detection dataset
https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud


