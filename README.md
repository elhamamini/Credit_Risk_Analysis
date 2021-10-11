# Credit_Risk_Analysis

## Overview of the analysis: 
Multiple methodologies and techniques are leveraged to predict credit risk using a dataset from LendingClub, which is a peer-to-peer lending services company. 

As credit risk is an  unbalanced classification problem where good loans signficantly outnumber risky loans, Python imbalanced-learn and scikit-learn libraries are used to build and evaluate models. Resampling algrotihms include RandomOverSampler, SMOTE, ClusterCentroids, and SMOTEENN.

To reduce bias, the BalancedRandomForestClassifier and EasyEnsembleClassifier machine learning models are also used to predict credit risk.  The performance of each model is compared and evaluated.
 
 The analysis process was broken down into
    - Preprocessing Data(Encoding, Splitting, Scaling)
    - Training and Testing
    - and Deploying the Models
    

**The Best Performing Model:**

Overall looking at all the metrics, the model that performed the best was, 'Easy Ensemble Adaboost
Classifier', with highest F1 score (for high-risk) of 0.16, highest F1 score (for low-risk) of 0.97 and the best accuracy score of 0.93.

**The Lowest Performing Model:**

The model that didnt fare all that well realtive to others was undersampling with clustercentroids on logistic regression model. with lowest F1 of 0.4 (for high-risk), lowest F1 of 0.86 (for low-risk) and the second lowest balanced accuracy score of 0.82.

**The Best Performing Model minus Ensemble:**

the model that performed the best was, 'SMOTE', with relatively high F1 score (for high-risk) of 0.07,  relatively high F1 score (for low-risk) of 0.93 and a good balanced accuracy score of 0.84.

**Balanced Random Forest Classifier's top 3 contributing feature variables were:**

        -   0.079, 'total_rec_prncp'
        -   0.059, 'total_pymnt'
        -   0.056, 'total_pymnt_inv'
        
## Conclusion

The "Easy Ensemble Adaboost", was the best performing model in this analysis and is hence recommended. However, we need to keep in mind that due to its high recall value and low precision value, it will have high False Positives, meaning many low-risk loans might get labled as high-risk as well, and will require additional time, effort and resources to vet them out. So keeping this in mind the recommended model can be used as an initial screening which can be further inspected.
