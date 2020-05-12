# Problem Statement
A training institute which conducts training for analytics/ data science wants to expand their business to manpower recruitment (data science only) as well.
Company gets large number of signups for their trainings. Now, company wants to connect these enrollees with their clients who are looking to hire employees working in the same domain. Before that, it is important to know which of these candidates are really looking for a new employment. They have student information related to demographics, education, experience and features related to training as well.
To understand the factors that lead a person to look for a job change, the agency wants you to design a model that uses the current credentials/demographics/experience to predict the probability of an enrollee to look for a new job.

# Link Reference
https://datahack.analyticsvidhya.com/contest/janatahack-hr-analytics/


# Approach: 
To predict the probability of an enrollee to look for a new job I used XGB Classifier as the dataset was imbalanced and ensemble models are good at handling them.

Metric for judgement : ROC AUC

Test AUC obtained: 0.67 
