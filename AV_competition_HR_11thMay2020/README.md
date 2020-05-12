# Problem Statement
A training institute which conducts training for analytics/ data science wants to expand their business to manpower recruitment (data science only) as well.
Company gets large number of signups for their trainings. Now, company wants to connect these enrollees with their clients who are looking to hire employees working in the same domain. Before that, it is important to know which of these candidates are really looking for a new employment. They have student information related to demographics, education, experience and features related to training as well.
To understand the factors that lead a person to look for a job change, the agency wants you to design a model that uses the current credentials/demographics/experience to predict the probability of an enrollee to look for a new job.

# Dataset:  
Used Google colab as platform for coding. Fetched training and testing data using '!wget' inside notebook. 

# Link Reference
https://datahack.analyticsvidhya.com/contest/janatahack-hr-analytics/

# Learning from this:
Binning can reduce overfitting.
Use of sklearn's SimpleImputer both for categorical and numerical variables.
Handling of missing values and outliers! 
Finally training and testing dataset are manipulated at the same time by appending them together then again separating them    using : <dataframe_name>[<dataframe_name>[<'target_variable_name'>].isnull()!=True] will give us the training set back and 
<dataframe_name>[<dataframe_name>[<'target_variable_name'>].isnull()==True] will give us the test dataset back! The idea is basd on the fact when one appends the train and test dataset the test doesn't have the 'target' variable or the dependant variable but the train does which results in formation of NaN in certain places in the 'target' columns of the combined dataset. Manipulate the combined dataset as one likes and finally reverse engineering gives us  back our training and testing dataset. I found this technique from one of the contestants very time saving. So I implemented it later.(added in the notebook)

# Approach: 
To predict the probability of an enrollee to look for a new job I used XGB Classifier ( and LGBM but was not giving satisfactory results so I switched back to XGBClassifier ) as the dataset was imbalanced and ensemble models are good at handling them. I tried using SMOTENC on the training dataset but not much improvement because XGBClassifier was handling it well. 

Metric for judgement : ROC AUC

Test AUC obtained: 0.67 
