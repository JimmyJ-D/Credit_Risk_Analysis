# Module 17 | Challenge - Credit Risk
Using Python, Jupyter Notebook, and Supervised Machine Learning

## Background and Overview

Using supervised machine learning we will look at the world of credit risk to train models to predict and identify credit risk in lending.
All data was cleaned and target column values were converted to "low_risk" and "high_risk" based on their values. When using the data to train the models, we split the data into training and testing dataset to be applied to the algorithm. I use Random State of 1 for all models calculations.

We will apply six different models for the Lending-Club Credit Risk simulation. 

1. Naive Random Oversampling vs SMOTE
2. Undersampling using Cluster Centroids algorithm
3. Combination of (Over and Under) Sampling using the SMOTEENN algorithm
4. Balanced Random Forest Classifying
5. Easy Ensemble Classifying

![Split-Datagram](https://github.com/JimmyJ-D/Credit_Risk_Analysis/blob/main/Credit_Risk_Analysis/Resources/datagram.png)

## Naive Random Oversampling

- Accuracy Score - 64.9%
- Precision High Risk - 1%
- Precision Low Risk - 100%
- Recall High Risk - 63%
- Recall Low Risk - 67%
![Random-Over-Sample-Accuracy-Score](https://github.com/JimmyJ-D/Credit_Risk_Analysis/blob/main/Credit_Risk_Analysis/Resources/Random-Over-Sample-Accuracy-Score.png)
![Random-Over-Sample](https://github.com/JimmyJ-D/Credit_Risk_Analysis/blob/main/Credit_Risk_Analysis/Resources/Random%20Over%20Sample.png)

## SMOTE Oversampling

- Accuracy Score - 60.7%
- Precision High Risk - 1%
- Precision Low Risk - 100%
- Recall High Risk - 55%
- Recall Low Risk - 66%
![SMOTE-Over-Sampling-Accuracy-Score](https://github.com/JimmyJ-D/Credit_Risk_Analysis/blob/main/Credit_Risk_Analysis/Resources/SMOTEENN-Accuracy-Score.png)
![SMOTE-Over-Sampling](https://github.com/JimmyJ-D/Credit_Risk_Analysis/blob/main/Credit_Risk_Analysis/Resources/SMOTEENN-Sampling.png)

## Cluster Centriods Undersampling

- Accuracy Score - 54.4%
- Precision High Risk - 1%
- Precision Low Risk - 100%
- Recall High Risk - 55%
- Recall Low Risk - 71%
![SMOTE-Over-Sampling-Accuracy-Score](https://github.com/JimmyJ-D/Credit_Risk_Analysis/blob/main/Credit_Risk_Analysis/Resources/SMOTE-Over-Sampling-Accuracy-Score.png)
![SMOTE-Over-Sampling](https://github.com/JimmyJ-D/Credit_Risk_Analysis/blob/main/Credit_Risk_Analysis/Resources/SMOTE-Over-Sampling.png)

## Combination (Over and Under) Sampling SMOTEENN

- Accuracy Score - 62.5%
- Precision High Risk - 1%
- Precision Low Risk - 100%
- Recall High Risk - 71%
- Recall Low Risk - 54%
![SMOTEENN-Accuracy-Score](https://github.com/JimmyJ-D/Credit_Risk_Analysis/blob/main/Credit_Risk_Analysis/Resources/SMOTEENN-Accuracy-Score.png)
![SMOTEENN-Sampling](https://github.com/JimmyJ-D/Credit_Risk_Analysis/blob/main/Credit_Risk_Analysis/Resources/SMOTEENN-Sampling.png)

## Balanced Random Forest Classifier

- Accuracy Score - 78.7%
- Precision High Risk - 4%
- Precision Low Risk - 100%
- Recall High Risk - 67%
- Recall Low Risk - 91%
![Balanced-Random-Forest-Classifier-Accuracy-Score](https://github.com/JimmyJ-D/Credit_Risk_Analysis/blob/main/Credit_Risk_Analysis/Resources/Balanced-Random-Forest-Classifier-Accuracy-Score.png)
![Balanced-Random-Forest-Classifier](https://github.com/JimmyJ-D/Credit_Risk_Analysis/blob/main/Credit_Risk_Analysis/Resources/Balanced-Random-Forest-Classifier.png)

## Easy Ensemble AdaBoost Classifier

- Accuracy Score - 92.5%
- Precision High Risk - 7%
- Precision Low Risk - 100%
- Recall High Risk - 91%
- Recall Low Risk - 94%
![Easy-Ensemble-AdaBoost-Classifier-Accuracy-Score](https://github.com/JimmyJ-D/Credit_Risk_Analysis/blob/main/Credit_Risk_Analysis/Resources/Easy-Ensemble-AdaBoost-Classifier-Accuracy-Score.png)
![Easy-Ensemble-AdaBoost-Classifier](https://github.com/JimmyJ-D/Credit_Risk_Analysis/blob/main/Credit_Risk_Analysis/Resources/Easy-Ensemble-AdaBoost-Classifier.png)


## Summary
When building models to examine datasets we have to understand what the models are showing us. Lending-Club would like to find a model that isolates or account for the least amount of high risk loans passing the algorithm undetected. Examining the "Recall High Risk" percentage rate, Easy Ensemble AdaBoost performed the best with a 91% recall rate followed by Over and Under Sampling SMOTEENN model. When running models they will produce false positive or for us low risk loan that are tagged has high risk, so that the loan is not approved. This will cause the company to lose potential customers. We need to examine the "Recall rate for Low Risk", we would like for this percentage to high so that low risk loans are not mistakenly denied  The Easy Ensemble AdaBoost Classifier has 94% Recall Low Risk rate. Using the dataset from Lending-Club and running all six models, I would recommend Easy Ensemble AdaBoost Classifier. The model has the highest accuracy scores and is able to mitigate the number of low risk loan being rejected.   
