# Credit_Risk_Analysis
Supervised Machine Learning

## Analysis and Purpose
This project has been undertaken on behalf of "Fast Lending", a fictitious peer to peer lending services company that uses machine learning to predict credit risk. Credit Risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, different techniques have been employed to train and evaluate models with unbalanced classes. This analysis includes evaluating several models to understand their efficiency to predict credit risk.

## Resources
- Data : LoanStats_2019Q1.csv
- Software : Python, Jupyter Notebook

## Results

### 1.Random Oversampling Model

![](images/accuracy_score_random_oversampling.png)

![image](https://user-images.githubusercontent.com/102105537/183309747-cf389f03-1af3-4e32-9846-eb4e3a6cb8f2.png)

![](images/random_oversampling_classification_report.png)

#### Observations

1. The balanced accuracy score of the Random Oversampling Model is approximately 63%
2. The precision for high-risk loans is very low at .01 and very high for low-risk loans at 1
3. The recall for high-risk loans is around .57 and it is  .68 for low-risk loans


 ### 2.SMOTE Oversampling Model
 
 ![](images/acc_score_SMOTE.png)
 
 ![](images/SMOTE_Oversampling_cm.png)
 
 ![](images/SMOTE_Oversampling_CR.png)
 
 #### Observations
 
 1. The balanced accuracy score for the SMOTE model is approximately 63%.
 2. The precision is low for high-risk loans at .01 and high for low risk loans at 1
 3. The recall is similar for both high-risk and low-risk loans at approximately .63

### 3.Cluster Centroids Undersampling Model

![](images/acc_Score_CC.png)

![](images/CC_Undersampling_CM.png)

![](images/CC_Undersampling_CR.png)

#### Observations

1. The balanced accuracy score for the Cluster Centroids Undersampling model is approximately 52%
2. The precision is very low for high-risk loans and very high for low-risk loans at .01 and 1 respectively
3. The recall for high-risk loans is around .57 and for low-risk loans is around .46


### 4.SMOTEENN Model

![](images/acc_score_SMOTEENN.png)

![](images/SMOTEENN_CM.png)

![](images/SMOTEENN_CR.png)

#### Observations

1. The balanced accuracy score of this model is approximately 62%
2. The precision is very low for high-risk loans and very high for low-risk loans at .01 and 1 respectively
3. The recall for high-risk loans is around .7 and for low-risk loans is around .54


### 5.BalancedRandomForestClassifier Model

![](images/acc_score_brfc.png)

![](images/brfc_CM.png)

![](images/brfc_CR.png)

#### Observations

1. The balanced accuracy score for this model is approximately 79%
2. The precision for high-risk loans is approximately .04 and for low-risk loans is 1
3. The recall for high-risk loans is approximately .67 and for low-risk loans is approximately .91


### 6.EasyEnsembleClassifier Model

![](images/acc_score_EEC.png)
![](images/eec_CM.png)
![](images/eec_CR.png)

#### Observations

1. The balanced accuracy score for this model is approximately 93%
2. The precision for high-risk loans is approximately .07 and 1 for low-risk loans
3. The recall for high-risk loans is approximately .91 and .94 for low-risk loans


**Note**

- *Precision is the measure of how reliable a positive classification is. A low precision is indicative of a large number of false positives.*

- *Recall is the ability of the classifier to find all the positive samples. A low recall is indicative of a large number of false negatives.*

## Summary

All the models used to perform the credit risk analysis show low precision in determining high-risk loans. The ensemble models did a better job overall compared to the resampling models. Out of the 6 machine learning models used, the EasyEnsemble Classifier model shows an accuracy score of 93% with high recall rates of .91 and .94 for high-risk and low-risk loans respectively, which means that this model is able to correctly identify the high-risk cases. Therefore, I would recommend using the EasyEnsemble Classifier model over the others. However, one downside of this model is that it has a low precision rate for high-risk cases which means there are many false positive cases. But in this scenario, I believe higher sensitivity is more important than precision because it is better for the company to wrongly classify low-risk cases as high-risk than have high-risk applicants classified as low-risk. The company can further analyze the high-risk cases before reaching a conclusion.
