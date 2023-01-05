# Credit Risk Analysis
## Overview of the loan prediction risk analysis:
  In this analysis, we are working with a peer-to-peer lending service company to predict credit card risk. We will specifically be using Machine Learning to help make a more reliable experience with less risk for people defaulting on loans by selecting better candidates. However, the data we have has many more low risk loans than high risk loans available, and we want our data to reflect an equal amount of both reduce bias and produce the most accurate predictions. We will use Supervised Machine Learning because we are using data where we already know the outcome of the candidates and their variables, and we will use this data to predict other candidates very quickly. In order to have sample testing that is unbias, we will test the data using multiple algorithms that use different statistical algorithms to give us same size sample data. The following algothims will be used:
- RandomOverSampler
- SMOTE algorithms
- ClusterCentroids algorithm
- SMOTEENN algorithm
- BalancedRandomForestClassifier (bias reduction model)
- EasyEnsembleClassifier (bias reduction model)

  To do this, we split our sample data into 4 groups.
**X_train:** A large portion of the data which we will use on our algorithms to make precitions. It includes all independent variables in the data set **EXCEPT** loan status.
**X_test:** A small portion of the data which will be used against the results to point out accuracy. It includes all independent variables in the data set **EXCEPT** loan status.
**Y_train:** A large portion of the data which has the dependent variable to the data independent variables in X_train and will assist in making accurate predictions in the model. This includes **ONLY** the loan status.
**Y_test:** A small portion of the data which has the dependent variable to the data sets and is used to test the prediction answers against "new" data.

  After each algorithm is applied to the dataset, we will use Both a Balanced Accuracy Score AND Imbalanced Classification Report to display the precision and recall for each test. The following are definitions:
**Balanced Accuracy Score:** *what was the percent of correctly predicted outcomes?*
**Precision:** *What percent were True Positives?*
**Recall:** *What is the percent of correct positive predictions out of all positive predictions?*
  The results from each algorithm will then help us determine the best one to apply to the quick peer-to-peer lending company to reduce risk for lenders and protect the customers from getting approved for loans they cannot pay.
  
## Results:

There is a bulleted list that describes the balanced accuracy score and the precision and recall scores of all six machine learning models (15 pt)
### - RandomOverSampler
![image](photos/.png)
**balanced accuracy score:**
**precision:**
**recall:**
### - SMOTE algorithms
![image](photos/.png)
**balanced accuracy score:**
**precision:**
**recall:**
### - ClusterCentroids algorithm
![image](photos/.png)
**balanced accuracy score:**
**precision:**
**recall:**
### - SMOTEENN algorithm
![image](photos/.png)
**balanced accuracy score:**
**precision:**
**recall:**
### - BalancedRandomForestClassifier (bias reduction model)
![image](photos/.png)
**balanced accuracy score:**
**precision:**
**recall:**
### - EasyEnsembleClassifier (bias reduction model)
![image](photos/.png)
**balanced accuracy score:**
**precision:**
**recall:**
## Summary:
There is a summary of the results (2 pt)
There is a recommendation on which model to use, or there is no recommendation with a justification (3 pt)
