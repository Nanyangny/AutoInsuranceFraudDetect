# AutoInsuranceFraudDetect


Auto Insurance Fraud detection Project

Data exploration analysis

Check correlation, remove unimportant features
plot graphs to check relation between non-number features and the fraud_Reported

Data_cleaning
Standardize data type
Fill up NA data (min, max, mean, median)
Standardise the data (strings -> categorial data)


Feature engineering [One of the most important steps!!]
Convert existing columns to ones that are more meaningful for learning
[ auto_year -> vehicle age ]
[ncident_hour_of_the_day -> using bins to cut them into period of a day]

Further research on the feature engineering techniques
  
Data Type
Feature engineering
techniques
Remarks
Continuous numeric data
Count/ Frequency
Combined the ones with the same ID
Binarize
Yes/No to some questions
Rounding numbers	
Get the percentage of some features instead of keeping the original numbers
correlation
Create new features by multiplying, squre, square root features (can be to itself or with other features)
Cut into bins
Segment the data, like the time of incidence in the auto insurance dataset, we are not interested in knowing the exact timing of the incident, in fact the period of when it happens is more useful for us.
Intervalize 
Set a same interval for data, get the categorization, applicable to ages, if we want to find out age groups. 
Can self-define, or do it by quartiles
log


Help to stablize the loss with the its normalization ability 
Categorial data
(nominal /Ordinal)



Ordinal -> number 





One-hot encoding
/Get_dummies/ effect coding scheme
for nominal categorial data
Feature hashing scheme
To solve curse of dimensionality


Select the features for training 
Check missing data of a column, drop those with high percentage of missing values(it depends on the context)
One-hot encoding for those categorial data
Concat selected data together 
Normalisation

Selection of models 
Split data set into training and testing
preliminary training using a base-model to benchmark the accuracy
Train data on multiple suitable models

LDA
Random Forest Tree
KNN
Decision Tree
AdaBoost
SVC
XGBoost
Logistic Regression

Compare performance based on accuracy / precision first

Select one or two best models to further optimise the learning
Use Grid Search CV to search for the best set of parameter

Research on other grid search methods

Evaluation and presentation
Basic performance metric 
Recall/Precision/ Accuracy/ F1-score
AUC and ROC curve 



