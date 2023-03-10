# Credit Risk Analysis
## Overview of the loan prediction risk analysis:
  In this analysis, we are working with a peer-to-peer lending service company to predict credit card risk. We will specifically be using Machine Learning to help make a more reliable experience with less risk for people defaulting on loans by selecting better candidates. However, the data we have has many more low risk loans than high risk loans available, and we want our data to reflect an equal amount of both reduce bias and produce the most accurate predictions. We will use Supervised Machine Learning because we are using data where we already know the outcome of the candidates and their variables, and we will use this data to predict other candidates very quickly. In order to have sample testing that is unbias, we will test the data using multiple algorithms that use different statistical algorithms to give us same size sample data. The following algothims will be used:
- ```RandomOverSampler```
- ```SMOTE``` algorithms
- ```ClusterCentroids``` algorithm
- ```SMOTEENN``` algorithm
- ```BalancedRandomForestClassifier``` (bias reduction model)
- ```EasyEnsembleClassifier``` (bias reduction model)</br>
</br>

To do this, we split our sample data into 4 groups.</br>
**```X_train```:** A large portion of the data which we will use on our algorithms to make precitions. It includes all independent variables in the data set **EXCEPT** loan status.</br>
**```X_test```:** A small portion of the data which will be used against the results to point out accuracy. It includes all independent variables in the data set **EXCEPT** loan status.</br>
**```Y_train```:** A large portion of the data which has the dependent variable to the data independent variables in X_train and will assist in making accurate predictions in the model. This includes **ONLY** the loan status.</br>
**```Y_test```:** A small portion of the data which has the dependent variable to the data sets and is used to test the prediction answers against "new" data.</br>

  After each algorithm is applied to the dataset, we will use Both a Balanced Accuracy Score AND Imbalanced Classification Report to display the precision and recall for each test. The following are definitions:</br>
**Balanced Accuracy Score:** *what was the percent of correctly predicted outcomes?*</br>
**Precision:** *What percent were True Positives?*</br>
**Recall:** *What is the percent of correct positive predictions out of all positive predictions?*</br>
  The results from each algorithm will then help us determine the best one to apply to the quick peer-to-peer lending company to reduce risk for lenders and protect the customers from getting approved for loans they cannot pay.</br>
  
## Results:

### - ```RandomOverSampler```
![image](photos/oversampling.png)</br>
**balanced accuracy score:** 0.6447 </br>
**precision:** *high risk* -> 0.01 *low risk* -> 1.00 </br>
**recall:** *high risk* -> 0.70 *low risk* -> 0.59 </br>
### - ```SMOTE``` algorithms
![image](photos/SMOTE.png)</br>
**balanced accuracy score:** 0.6623 </br>
**precision:** *high risk* -> 0.01 *low risk* -> 1.00 </br>
**recall:** *high risk* -> 0.63 *low risk* -> 0.69 </br>
### - ```ClusterCentroids``` algorithm
![image](photos/cluster.png)</br>
**balanced accuracy score:** 0.5442 </br>
**precision:** *high risk* -> 0.01 *low risk* -> 1.00 </br>
**recall:** *high risk* -> 0.67 *low risk* -> 0.42 </br>
### - ```SMOTEENN``` algorithm
![image](photos/SMOTEENN.png)</br>
**balanced accuracy score:** 0.6531 </br>
**precision:** *high risk* -> 0.01 *low risk* -> 1.00 </br>
**recall:** *high risk* -> 0.73 *low risk* -> 0.57 </br>
### - ```BalancedRandomForestClassifier``` (bias reduction model)
![image](photos/brf.png)</br>
**balanced accuracy score:** 0.7885 </br>
**precision:** *high risk* -> 0.03 *low risk* -> 1.00 </br>
**recall:** *high risk* -> 0.70 *low risk* -> 0.87 </br>
### - ```EasyEnsembleClassifier``` (bias reduction model)
![image](photos/eec.png)</br>
**balanced accuracy score:** 0.9317 </br>
**precision:** *high risk* -> 0.09 *low risk* -> 1.00 </br>
**recall:** *high risk* -> 0.92 *low risk* -> 0.94 </br>
## Summary:
  Based on the results of the six algothrithms,```EasyEnsembleClassifer``` was clearly the best fit alogothrim at finding "High Risk" loans since it found 93% of the total predictions correctly, 9% of true positives were "High Risk" and 92% of them were correctly found. ```BalancedRansomForectClassifier``` found 79% of the total predictions correctly, 3% of the true positves were "High Risk" but only 70% of them were correctly found. ```SMOTEEN``` found 65% of the total predictions correctly, 1% of the true positves were "High Risk" and 73% of them were correctly found. ```RandomOverSampler``` found 64% of the total predictions correctly, only 1% of the true positves were "High Risk" but 70% of them were correctly found. ```SMOTE``` found 66% of the total predictions correctly, only 1% of the true positves were "High Risk" and 63% of them were correctly found. ```ClusterCentroids``` only found 54% of the total predictions correctly, only 1% of the true positves were "High Risk", but it was slightly better than ```SMOTE``` at finding them, 67% of them were correctly found.
  Although the ```EasyEnsembleClassifer``` was the best algothrithm for finding "High Risk" loans, the lending company should consider the fact that the dataset only contained 0.5% "High Risk" loans. The company should consider if this dataset is reflective of the national or state-wide average, depending on the area they will be in. Perhaps another dataset or scraping more data into the current set would then create a stronger prediction rate. If the company is aiming for around 9% of their loan applicants to be "High Risk", then we can sufficiently say we have found a strong Supervised Machine Learning algorithm with the ```EasyEnsembleClassifier```. 
