# Credit Risk Analysis
## Overview
The purpose of this analysis is to use a variety of techniques to evaluate and predict credit risk using a dataset from LendingClub.

## Results
### Random OverSampling Model
- **Accuracy Score:** 0.6463970560994359
  - This model was correct 64.6% of the time


![Image](https://github.com/MDHetrick/Credit_Risk_Analysis/blob/main/Resources/ROS_AS.png)


- **Confusion Matrix:** 
```         
array([[  72,   29],
         [7185, 9919]], dtype=int64)                               
```
![Image](https://github.com/MDHetrick/Credit_Risk_Analysis/blob/main/Resources/ROS_CM.png)

- **Imbalanced Classification Report:**
```
                   pre       rec       spe        f1       geo       iba       sup

  high_risk       0.01      0.71      0.58      0.02      0.64      0.42       101
   low_risk       1.00      0.58      0.71      0.73      0.64      0.41     17104

avg / total       0.99      0.58      0.71      0.73      0.64      0.41     17205
```
![Image](https://github.com/MDHetrick/Credit_Risk_Analysis/blob/main/Resources/ROS_CR2.png)


### SMOTE
- **Accuracy Score:**  0.6586230769943224

![Image](https://github.com/MDHetrick/Credit_Risk_Analysis/blob/main/Resources/S_AS2.png)

- **Confusion Matrix:** 
```
array([[   64,    37],
       [ 5412, 11692]], dtype=int64)
```

![Image](https://github.com/MDHetrick/Credit_Risk_Analysis/blob/main/Resources/S_CM2.png)

- **Imbalanced Classification Report:**
```
                   pre       rec       spe        f1       geo       iba       sup

  high_risk       0.01      0.63      0.68      0.02      0.66      0.43       101
   low_risk       1.00      0.68      0.63      0.81      0.66      0.44     17104

avg / total       0.99      0.68      0.63      0.81      0.66      0.44     17205
```

![Image](https://github.com/MDHetrick/Credit_Risk_Analysis/blob/main/Resources/S_CR2.png)


### Cluster Centroids

- **Accuracy Score:** 0.5439153831192286
  - This model was correct 54.4% of the time
  
  
![Image](https://github.com/MDHetrick/Credit_Risk_Analysis/blob/main/Resources/CC_AS2.png)

- **Confusion Matrix:** 
```
array([[   70,    31],
       [10352,  6752]], dtype=int64)
```

![Image](https://github.com/MDHetrick/Credit_Risk_Analysis/blob/main/Resources/CC_CM2.png)

- **Imbalanced Classification Report:**
```
                   pre       rec       spe        f1       geo       iba       sup

  high_risk       0.01      0.69      0.39      0.01      0.52      0.28       101
   low_risk       1.00      0.39      0.69      0.57      0.52      0.27     17104

avg / total       0.99      0.40      0.69      0.56      0.52      0.27     17205

```

![Image](https://github.com/MDHetrick/Credit_Risk_Analysis/blob/main/Resources/CC_CR2.png)

### Predicting Credit Risk using SMOTEEN
- **Accuracy Score:** 0.6361059077142514
  - This model was correct 63.6% of the time


![Image](https://github.com/MDHetrick/Credit_Risk_Analysis/blob/main/Resources/SM_AS.png)


- **Confusion Matrix:** 
```
array([[   69,    32],
       [ 7029, 10075]], dtype=int64)
```
![Image](https://github.com/MDHetrick/Credit_Risk_Analysis/blob/main/Resources/SM_CM.png)

- **Imbalanced Classification Report:**
```
                   pre       rec       spe        f1       geo       iba       sup

  high_risk       0.01      0.68      0.59      0.02      0.63      0.41       101
   low_risk       1.00      0.59      0.68      0.74      0.63      0.40     17104

avg / total       0.99      0.59      0.68      0.74      0.63      0.40     17205
```
![Image](https://github.com/MDHetrick/Credit_Risk_Analysis/blob/main/Resources/SM_CR.png)


### Balanced Random Forest Classifier
- **Accuracy Score:** 0.7885466545953005
  - This model was correct 78.8% of the time


![Image](https://github.com/MDHetrick/Credit_Risk_Analysis/blob/main/Resources/BRFC_AS.png)

- **Confusion Matrix:** 
```
array([[   71,    30],
       [ 2153, 14951]], dtype=int64)
```

![Image](https://github.com/MDHetrick/Credit_Risk_Analysis/blob/main/Resources/BRRC_CM.png)

- **Imbalanced Classification Report:**
```
                   pre       rec       spe        f1       geo       iba       sup

  high_risk       0.03      0.70      0.87      0.06      0.78      0.60       101
   low_risk       1.00      0.87      0.70      0.93      0.78      0.62     17104

avg / total       0.99      0.87      0.70      0.93      0.78      0.62     17205
```
![Image](https://github.com/MDHetrick/Credit_Risk_Analysis/blob/main/Resources/BRFC_CR.png)

- **Feature sorting by importance:**


![Image](https://github.com/MDHetrick/Credit_Risk_Analysis/blob/main/Resources/BRFC_DF.png)


### Easy Ensemble Classifier
- **Accuracy Score:** 0.9316600714093861
  - This model was correct 93.2% of the time


![Image](https://github.com/MDHetrick/Credit_Risk_Analysis/blob/main/Resources/EEC_AS.png)

- **Confusion Matrix:** 
```
array([[   93,     8],
       [  983, 16121]], dtype=int64)
```

![Image](https://github.com/MDHetrick/Credit_Risk_Analysis/blob/main/Resources/EEC_CM.png)

- **Imbalanced Classification Report:**
```
                   pre       rec       spe        f1       geo       iba       sup

  high_risk       0.09      0.92      0.94      0.16      0.93      0.87       101
   low_risk       1.00      0.94      0.92      0.97      0.93      0.87     17104

avg / total       0.99      0.94      0.92      0.97      0.93      0.87     17205
```

![Image](https://github.com/MDHetrick/Credit_Risk_Analysis/blob/main/Resources/EEC_CR.png)

## Summary
### Accuracy Scores
- Based on the accuracy scores, the easy ensemble classifier model was optimal, with an accuracy score of 93.2%. All accuracy scores are shown below
  - **Random OverSampling:** 0.6464
  - **SMOTE:**  0.6586
  - **Cluster Centroids:** 0.5439
  - **SMOTEEN:** 0.6361
  - **Balanced Random Forest Classifier:** 0.7885
  - **Easy Ensemble Classifier:** 0.9317
### Confusion Matrices
-  Based on the confusion matrices, the the easy ensemble classifier model has the fewest falsely classified
  - **Random OverSampling Model:** 
```        
array([[  72,   29],
         [7185, 9919]], dtype=int64)                               
```
  - **SMOTE:** 
```
array([[   64,    37],
       [ 5412, 11692]], dtype=int64)
```

  - **Cluster Centroids:** 
```
array([[   70,    31],
       [10347,  6757]], dtype=int64)
```
  - **SMOTEEN:** 
```
array([[   69,    32],
       [ 7029, 10075]], dtype=int64)
```
  - **Balanced Random Forest Classifier:** 
```
array([[   71,    30],
       [ 2153, 14951]], dtype=int64)
```
  - **Easy Ensemble Classifier:** 
```
array([[   93,     8],
       [  983, 16121]], dtype=int64)
```
### Imbalanced Classification Reports
#### Precision Scores
- The avg/total precision was the same (0.99) for all models and the low risk category (1.00), while precision of the high risk category was highest with the easy ensemble classifier (0.09).
- **Random OverSampling:** 
  - Avg/total: 0.99
  - high risk: 0.01
  - low risk: 1.00
- **SMOTE:**  
  - Avg/total: 0.99
  - high risk: 0.01
  - low risk: 0.01
- **Cluster Centroids:** 
  - Avg/total: 0.99
  - high risk: 0.01
  - low risk: 1.00
- **SMOTEEN:** 
  - Avg/total: 0.99
  - high risk: 0.01
  - low risk: 0.99
- **Balanced Random Forest Classifier:** 
  - Avg/total: 0.99 
  - high risk: 0.03
  - low risk: 1.00
- **Easy Ensemble Classifier:** 
  - Avg/total: 0.99
  - high risk: 0.09
  - low risk: 1.00
#### Recall Scores
- The easy ensemble classifier model has the highest recall of all categories 
- **Random OverSampling:** 
  - Avg/total: 0.58
  - high risk: 0.71
  - low risk: 0.58
- **SMOTE:**  
  - Avg/total: 0.68 
  - high risk: 0.63
  - low risk: 0.68
- **Cluster Centroids:** 
  - Avg/total: 0.40
  - high risk: 0.69
  - low risk: 0.39
- **SMOTEEN:** 
  - Avg/total: 0.59
  - high risk: 0.68
  - low risk: 0.59
- **Balanced Random Forest Classifier:** 
  - Avg/total: 0.70
  - high risk: 0.87
  - low risk: 0.70
- **Easy Ensemble Classifier:** 
  - Avg/total: 0.94
  - high risk: 0.92
  - low risk: 0.94
#### F1 (harmonic mean)
- The easy ensemble classifier model has the highest harmonic mean of all models
- **Random OverSampling:** 
  - Avg/total: 0.73
  - high risk: 0.02
  - low risk: 0.73
- **SMOTE:**  
  - Avg/total: 0.81
  - high risk: 0.02
  - low risk: 0.81
- **Cluster Centroids:** 
  - Avg/total: 0.56
  - high risk: 0.01
  - low risk: 0.57
- **SMOTEEN:** 
  - Avg/total: 0.74
  - high risk: 0.02
  - low risk: 0.74
- **Balanced Random Forest Classifier:** 
  - Avg/total: 0.93
  - high risk: 0.06
  - low risk: 0.93
- **Easy Ensemble Classifier:** 
  - Avg/total: 0.97
  - high risk: 0.16
  - low risk: 0.97
#### Classification Report Summary
The easy ensemble classifier model has the highest recall, f1(harmonic mean), and  low risk precision, indicating this model has more correctly categorized predictions than the other models. 
### Conclusion:
Using the information obtained from the accuracy scores, confusion matrices, and imbalanced classification reports, the easy ensemble classifier model outperforms the other models in this analysis.
