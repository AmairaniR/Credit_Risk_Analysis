# Credit_Risk_Analysis

## Overview 

An analysis of six different machine learning models (RandomOverSampler, SMOTE, ClusterCentroids, SMOTEENN, BalancedRandomForestClassifier, and EasyEnsembleClassifier) using imbalanced-learn and scikit-learn to determine which of the six models does best at rectifying the imbalance and reducing the bias of the loan dataset to better predict high credit card risk. 

## Results 

Accuracy scores and classification reports for all six models.

-RandomOverSampler

-low or less than satisfactory accuracy score ![ros_acc_score](https://github.com/AmairaniR/Credit_Risk_Analysis/blob/main/images/ros_acc_score.png) 

-low recall score in both high and low risk categories ![ros_classification_report](https://github.com/AmairaniR/Credit_Risk_Analysis/blob/main/images/ros_classification_report.png)


-SMOTE

-low or less than satisfactory accuracy score ![smote_acc_score](https://github.com/AmairaniR/Credit_Risk_Analysis/blob/main/images/smote_acc_score.png)

-slightly higher recall score in both high and low risk categories compared to the RandomOverSampler model but it is still insufficient for detecting high credit card risk ![smote_classification_report](https://github.com/AmairaniR/Credit_Risk_Analysis/blob/main/images/smote_classification_report.png)


-ClusterCentroids

-lowest accuracy score of all the models ![cc_acc_score](https://github.com/AmairaniR/Credit_Risk_Analysis/blob/main/images/cc_acc_score.png)

-the only model where the low-risk recall was lower than the high-risk recall but both were still low and insufficient ![cc_classification_report](https://github.com/AmairaniR/Credit_Risk_Analysis/blob/main/images/cc_classification_report.png)


-SMOTEENN

-low accuracy score, comprable to that of the oversampling models ![smoteenn_acc_score](https://github.com/AmairaniR/Credit_Risk_Analysis/blob/main/images/smoteenn_acc_score.png)

-recall scores are also similar to the oversampling models ![smoteenn_classification_report](https://github.com/AmairaniR/Credit_Risk_Analysis/blob/main/images/smoteenn_classification_report.png)


-BalancedRandomForestClassifier

-second highest accuracy score of all the models ![brfc_acc_score](https://github.com/AmairaniR/Credit_Risk_Analysis/blob/main/images/rfc_acc_score.png)

-increased low-risk recall score, high-risk recall score similar to that of oversampling, SMOTEENN models ![brfc_acc_score](https://github.com/AmairaniR/Credit_Risk_Analysis/blob/main/images/rfc_classification_score.png)


-EasyEnsembleClassifier

-highest accuracy score ![eec_acc_score](https://github.com/AmairaniR/Credit_Risk_Analysis/blob/main/images/eec_acc_score.png)

-highest recall scores in both categories ![ecc_acc_score](https://github.com/AmairaniR/Credit_Risk_Analysis/blob/main/images/eec_classification_report.png)


## Summary

The low-risk category had high precision and high sensitivity across all models, indicating that the data may be overfitted. On the other hand, the precision was low across all models in the high-risk category indicating the precence of many false positives. However, since these models are intended to predict clients that may pose a high credit card risk, recall is a more important metric. False positives can be ruled out another way. Regardless, the low F1 score across all models also indicates a pronounced imbalanced between recall and precision. 

My recommendation would be retry the models after more high-risk data has been gathered. However, if this is not possible because of limited time, staffing, or a budget, the best model to use in this circumstance would be the EasyEnsembleClassifier as it provided the highest accuracy score and the highest recall score for the high-risk category. 
