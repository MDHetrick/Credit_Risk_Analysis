# Credit_Risk_Analysis
## Overview
The purpose of this analysis is to use a variety of techniques to evaluate and predict credit risk using a dataset from Lendingclub.

## Results
### Resampling Models
#### Random OverSampling Model
**Model Description**

The majority (high_risk) and minority (low_risk) classes are balanced as the model randomly adds instances of the minority class to the training set.


- **Accuracy Score:** 0.6463970560994359
  - This model was correct 64.6% of the time


![Image](https://github.com/MDHetrick/Credit_Risk_Analysis/blob/main/Resources/ROS_AS.png)


- **Confusion Matrix:** 
```         Predicted  Predicted
              T           F
Actual T  [[  72,        29],
Actual F    [7185,     9919]], dtype=int64) 
 
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
  - Precision (pre): AKA positive predictive value
  - Recall (rec): AKA sensitivity - measure of how many categorized are correct
  - F1 (harmonic mean): single summary statistic of precision and sensitivity - highest f1 is overall best model


#### SMOTE
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


#### Cluster Centroids

- **Accuracy Score:** 0.544061547759079
  - This model was correct 54.4% of the time
![Image](https://github.com/MDHetrick/Credit_Risk_Analysis/blob/main/Resources/CC_AS.png)

- **Confusion Matrix:** 
```
array([[   70,    31],
       [10347,  6757]], dtype=int64)
```

![Image](https://github.com/MDHetrick/Credit_Risk_Analysis/blob/main/Resources/CC_CM.png)

- **Imbalanced Classification Report:**
```
                   pre       rec       spe        f1       geo       iba       sup

  high_risk       0.01      0.69      0.40      0.01      0.52      0.28       101
   low_risk       1.00      0.40      0.69      0.57      0.52      0.27     17104

avg / total       0.99      0.40      0.69      0.56      0.52      0.27     17205
```

![Image](https://github.com/MDHetrick/Credit_Risk_Analysis/blob/main/Resources/CC_CR.png)

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

### Using Ensemble Classifiers to Predict Credit Risk
#### Balanced Random Forest Classifier
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


#### Easy Ensemble Classifier
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
- **Random OverSampling:** 0.6464
- **SMOTE:**  0.6361
- **Cluster Centroids:** 0.54406
- **SMOTEEN:** 0.6361059
- **Balanced Random Forest Classifier:** 0.7885
- **Easy Ensemble Classifier:** 0.93166



Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.
There is a summary of the results (2 pt)
There is a recommendation on which model to use, or there is no recommendation with a justification (3 pt)
