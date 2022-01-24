# Credit_Risk_Analysis
## Overview of Analysis
Per the module "Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans." This analysis is to apply machine learning  to review credi card risk. Because credit risk is an "unbalanced classification problem", different techniques are being utilized to train and evaluate these unbalanced classes. Oversampling, SMOTE (Synthetic Minority Oversampling), undersampling using ClusterCentroids, and SMOTEENN (Synthetic Minority Oversampling- Edited Nearest Neighbors[ENN]). Then 2 machine learning models are used to reduce bias: BalancedRandomForest and EasyEnsembleClassifier. 

## Resources
Jupyter Notebook 6.3.0, Mlenv, SKlearn, Pandas, Numpy, Pathlib, Python, were used in this analysis. The data set used is contained in the references as LoanStats_2019Q1.csv

## Results
The analysis brings in the data and runs a train-test-split on the data. 
### Oversampled
The analysis then turns to the data oversampled. The balanced accuracy score is .644. 
The classification report is shown below: 

![image](https://user-images.githubusercontent.com/90878901/150702718-367f38c3-f2e5-4644-8837-cdd40a05bfe4.png)

The classification shows that the precision on the high risk is very low, while low_risk has high precision, The recall of both high and low risk demostrates a .1difference in the sensistivty. The combined f1 is .74 but is .74 low risk while high risk is at .02. 

### SMOTE Oversampling
In SMOTE the balnaced accuracy score slightly improves to .663. 
The classification report is shown below: 

![image](https://user-images.githubusercontent.com/90878901/150702883-7a6e6c48-3e21-4b68-ada5-6847c475b06b.png)

Like in oversampling the high risk precision is very low and low risk very high. The recall is now even closer leaving a difference in sensitivity of  .06. The average f1 score also increases but demonstrates the difference seen in precision. 

### Undersampling
Using Undersampling the balanced accuracy score decreases to .545.
The undersampling classification is shown below:

![image](https://user-images.githubusercontent.com/90878901/150702993-7fa0a7df-126f-401c-a1f9-57372ac17135.png)

Same split is seen as before in the Oversampling and SMOTE models this modeling does make more of a change in the sensitivity difference between high and low risk. With .29 seperating the values. 

### SMOTEEN
When both Oversampling and Undersampling are combined the balanced accuarcy score is at .645
The SMOTEEN classification report is below:

![image](https://user-images.githubusercontent.com/90878901/150703101-b6e51988-00c2-49bf-8606-117742e8a8e6.png)

Similar pattern as demostrated in the other models is seen. 

### Difference between Ensemple Learners

#### Balanced Random Forest Classifier. 
Applying the balanced random forest classifier, results in a balanced accuracy score of .788. 
The classification report is as follows:

![image](https://user-images.githubusercontent.com/90878901/150703210-c51e7211-3ee8-4e05-b0aa-c458d0061522.png)

This shows a much higher combined f1 score than in the non-Ensemble Learners. 

#### Easy Ensemble AdaBoost Classifier
When the adaBoost classifier is applied the balanced accuracy score climbs to .932
Here is the classification report when the adaBoost classifier is used:

![image](https://user-images.githubusercontent.com/90878901/150703335-7e7e00d2-551d-4762-8d81-047a3f8fc95a.png)

This provides by far the best precision score for high risk though still significantly lower than low risk. This model preforms the best for sensitivity as seen in the recall scores. This model has the best F1 score. 

## Summary
The Easy Ensemble AdaBoost Classifier provided the best results of all models on this data set. Additional analysis could be performed by gathering more data to see how the Ada Boost classifier performs. This data set is limited to Q1 2019. Additional data will slow down the system significantly. Also the value 120 could be used instead of 100 to see if the performace maintains. 


