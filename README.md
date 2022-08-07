# Credit_Risk_Analysis
Supervised Machine Learning

## Analysis and Purpose
This project has been undertaken on behalf of "Fast Lending", a fictitious peer to peer lending services company that uses machine learning to predict credit risk. Credit Risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, different techniques have been employed to train and evaluate models with unbalanced classes. This analysis includes evaluating several models to understand their efficiency to predict credit risk.

## Resources
- Data : LoanStats_2019Q1.csv
- Software : Python, Jupyter Notebook

## Results

### 1.Random Oversampling Model

![image](https://user-images.githubusercontent.com/102105537/183309787-581277c4-a6cf-413f-8f1b-c74da5b2a750.png)

![image](https://user-images.githubusercontent.com/102105537/183309747-cf389f03-1af3-4e32-9846-eb4e3a6cb8f2.png)

![image](https://user-images.githubusercontent.com/102105537/183309818-65c2d5b4-7bbd-499a-b0b7-df996527643b.png)

#### Observations

1. The balanced accuracy score of the Random Oversampling Model is approximately 63%
2. The precision for high-risk loans is very low at .01 and very high for low-risk loans at 1
3. The recall for high-risk loans is around .62 and it is  .63 for low-risk loans


 ### 2.SMOTE Oversampling Model
 
 ![image](https://user-images.githubusercontent.com/102105537/183309903-9781167a-3bf7-43c9-b1e7-412b02436273.png)
 
 ![image](https://user-images.githubusercontent.com/102105537/183309919-60c17276-0019-4381-8880-d446dd4b2943.png)
 
 ![image](https://user-images.githubusercontent.com/102105537/183309936-137c1920-9ccb-41f0-b5ad-373801352106.png)
 
 #### Observations
 
 1. The balanced accuracy score for the SMOTE model is approximately 63%.
 2. The precision is low for high-risk loans at .01 and high for low risk loans at 1
 3. The recall is similar for both high-risk and low-risk loans at approximately .63

### 3.Cluster Centroids Undersampling 

#### Observations

1. The balanced accuracy score for the Cluster Centroids Undersampling model is approximately 52%
2. The precision is very low for high-risk loans and very high for low-risk loans at .01 and 1 respectively
3. The recall for high-risk loans is around .57 and for low-risk loans is around .46


### 4.SMOTEENN 

#### Observations

1. The balanced accuracy score of this model is approximately 62%
2. The precision is very low for high-risk loans and very high for low-risk loans at .01 and 1 respectively
3. The recall for high-risk loans is around .7 and for low-risk loans is around .54


### 5.BalancedRandomForestClassifier 

#### Observations

1. The balanced accuracy score for this model is approximately 79%
2. The precision for high-risk loans is approximately .04 and for low-risk loans is 1
3. The recall for high-risk loans is approximately .70 and for low-risk loans is approximately .87


### 6.EasyEnsembleClassifier 

#### Observations

1. The balanced accuracy score for this model is approximately 93%
2. The precision for high-risk loans is approximately .07 and 1 for low-risk loans
3. The recall for high-risk loans is approximately .92 and .94 for low-risk loans


**Note**

- *Precision is the measure of how reliable a positive classification is. A low precision is indicative of a large number of false positives.*

- *Recall is the ability of the classifier to find all the positive samples. A low recall is indicative of a large number of false negatives.*

## Summary

I utilized all of the models to determine the pergfomance of the credit risk analysis. The analysis shows low precision in determining high-risk loans. The models overall looked like there was a better job compared to the resampling models. Of the 6 machine learning models used, the EasyEnsemble Classifier model shows an accuracy score of 93% with high recall rates of .91 and .94 for high-risk and low-risk loans. This observation means that this model should be able to correctly identify the high-risk cases. I would recommend that using the EasyEnsemble Classifier model. The drawback to this model is that it has a low precision rate for high-risk cases which means there are many false positive cases. The company can further analyze the high-risk cases before reaching a conclusion.
