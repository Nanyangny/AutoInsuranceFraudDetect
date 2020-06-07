# AutoInsuranceFraudDetect

This is my very first time to implement a machin learning model.

The dataset is from [kaggle](https://www.kaggle.com/roshansharma/fraud-detection-in-insurance-claims)

Most of the code are inspired by [this article](https://medium.com/fraud-investigation-using-machine-learning/fraud-detection-insurance-29d00b521525) and [this article](https://medium.com/fraud-investigation-part-ii/fraud-investigation-part-ii-42062c471db1) and , with some modification on the features and presentation. I also added comments and my understanding on the original code. It is not good to just blindly copy and paste, I did it by studying the code first and undertand the logic and rationale behind each step. 

Below is a little summary of what I learned from the article and other related knowledges and pipelines of a machine learning project.

### Data exploration analysis

* Check correlation, remove unimportant features
* plot graphs to check relation between non-number features and the fraud_Reported

### Data_cleaning
* Standardize data type
* Fill up NA data (min, max, mean, median)
* Standardise the data (strings -> categorial data)


### Feature engineering [One of the most important steps!!]
* Convert existing columns to ones that are more meaningful for learning
[ auto_year -> vehicle age ]
[incident_hour_of_the_day -> using bins to cut them into period of a day]

* Further research on the feature engineering techniques
 
| Data Type                          | Feature engineering techniques                       | Remarks                                                                                                                                                                                                     |
|------------------------------------|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Continuous numeric data            | Count/ Frequency                                     | Combined the ones with the same ID                                                                                                                                                                          |
|                                    | Binarize                                             | Yes/No to some questions                                                                                                                                                                                    |
|                                    | Rounding numbers	                                     | Get the percentage of some features instead of keeping the original numbers                                                                                                                                 |
|                                    | correlation                                          | Create new features by multiplying, squre, square root features (can be to itself or with other features)                                                                                                   |
|                                    | Cut into bins                                        | Segment the data, like the time of incidence in the auto insurance dataset, we are not interested in knowing the exact timing of the incident, in fact the period of when it happens is more useful for us. |
|                                    | Intervalize                                          | Set a same interval for data, get the categorization, applicable to ages, if we want to find out age groups.  Can self-define, or do it by quartiles                                                        |
|                                    | log                                                  | Help to stablize the loss with the its normalization ability                                                                                                                                                |
| Categorial data (nominal /Ordinal) | Ordinal -> number                                    |                                                                                                                                                                                                             |
|                                    |  One-hot encoding /Get_dummies/ effect coding scheme | for nominal categorial data                                                                                                                                                                                 |
|                                    | Feature hashing scheme                               | To solve curse of dimensionality                                                                                                                                                                            |


### Select the features for training 
* Check missing data of a column, drop those with high percentage of missing values(it depends on the context)
* One-hot encoding for those categorial data
* Concat selected data together 
* Normalisation

### Selection of models 
* Split data set into training and testing
* preliminary training using a base-model to benchmark the accuracy
* Train data on multiple suitable models

- LDA
- Random Forest Tree / Decision Tree
- KNN
- AdaBoost
- SVC
- XGBoost
- Logistic Regression

Compare performance based on accuracy / precision first

### Select one or two best models to further optimise the learning
Use Grid Search CV / Random Search CV to search for the best set of parameter


### Evaluation and presentation
Basic performance metric 
Recall/Precision/ Accuracy/ F1-score
AUC and ROC curve 


### Limitation

I think it would be better to do grid search for Logistic Regression as well to further improve the model


