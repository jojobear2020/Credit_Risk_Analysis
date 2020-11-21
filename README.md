# Credit_Risk_Analysis

## Analysis Purpose

TBU

## Important Metrics 

1.	*pre* – precision, which is a measure of result relevancy;
2.	*rec* – recall, which is the same as sensitivity. Recall is a measure of how many truly relevant results are returned;
3.	*spe* – specificity;
4.	*f1* – harmonic average of the precision and recall;
5.	*geo* – geometric mean of specificity and sensitivity;
6.	*iba* – index of imbalanced accuracy.

## Machine Learning Models

### 1. Naive Random Oversampling

* The accuracy score of 0.650 is quite low. The number represents the sum of diagonals of the confusion matric divided by the total test sample size of 17205.
* Overall precision score is 0.99.
* High risk has extremely low precision of 0.01 and we cannot rely on its results in this particular case.
* Low risk has a high precision level of 1.0.
* Despite high precision for low risk credit card, only about 61% (10433) would be predicted false.

***Confusion Matrix***

* Out of the 101 actual instances (first row), the classifier predicted correctly 70 of them.
* Out of the 17104 actual instances (second row), the classifier predicted correctly 10393 of them
* Out of sample of 17205, the classifier predicted correctly about 10463 of them. 


![]( https://github.com/jojobear2020/Credit_Risk_Analysis/blob/main/images/naive_random_oversampling_all.PNG)

____________________________


### 2. SMOTE Oversampling

•	The accuracy score of 0.662 is quite low.
•	Overall precision score is 0.99.
•	High risk has extremely low precision of 0.01 and we cannot rely on its results in this particular case (identical to Naïve Random Oversampling).
•	Low risk has a high precision level of 1.0.
•	Despite high precision for low risk credit card, only about 69% (11802) would be predicted true positive.

***Confusion Matrix***
•	 Out of the 101 actual instances (first row), the classifier predicted correctly 64 of them.
•	Out of the 17104 actual instances (second row), the classifier predicted correctly 11813 of them
•	Out of sample of 17205, the classifier predicted correctly about 11877 of them. 

![]( https://github.com/jojobear2020/Credit_Risk_Analysis/blob/main/images/smote_oversampling_all.PNG)

__________________________

### 3. Undersampling

* The accuracy score of 0.662 is quite low (very close to SMOTE).
* Overall precision score is 0.99.
* High risk has extremely low precision of 0.01 and we cannot rely on its results in this particular case (identical to Naïve Random Oversampling).
* Low risk has a high precision level of 1.0.
* Despite high precision for low risk credit card, only about 42% (7184) would be predicted true positive.

***Confusion Matrix***

* Out of the 101 actual instances (first row), the classifier predicted correctly 68 of them.
* Out of the 17104 actual instances (second row), the classifier predicted correctly 7100 of them
* Out of sample of 17205, the classifier predicted correctly about 7168 of them. 


![]( https://github.com/jojobear2020/Credit_Risk_Analysis/blob/main/images/undersampling_all.PNG)

_____________________________

### 4. SMOTEENN

* The accuracy score of 0.544 is very low (lowest by far).
* Overall precision score is 0.99.
* High risk has extremely low precision of 0.01 and we cannot rely on its results in this particular case (identical to Naïve Random Oversampling).
* Low risk has a high precision level of 1.0.
* Despite high precision for low risk credit card, only about 57% (9750) would be predicted true positive.

***Confusion Matrix***

* Out of the 101 high risk instances (first row), the classifier predicted correctly 79 of them.
* Out of the 17104 low risk instances (second row), the classifier predicted correctly 9795 of them
* Out of sample of 17205, the classifier predicted correctly about 9874 of them. 


![]( https://github.com/jojobear2020/Credit_Risk_Analysis/blob/main/images/smoteenn_all.PNG)

______________________

### 5. Balanced Random Forest Classifier

* The accuracy score of 0.788.
* Overall precision score is 0.99.
* High risk has extremely low precision of 0.03 (higher than prior 4 models, but we still cannot rely on its results in this particular case.
* Low risk has a high precision level of 1.0.
* Despite high precision for low risk credit card, about 87% (14880) would be predicted true positive.

***Confusion Matrix***

* Out of the 101 high risk instances (first row), the classifier predicted correctly 79 of them.
* Out of the 17104 low risk instances (second row), the classifier predicted correctly 9795 of them.
* Out of sample of 17205, the classifier predicted correctly about 9896 of them. 


![](https://github.com/jojobear2020/Credit_Risk_Analysis/blob/main/images/balanced_random_forester_classifier_all.PNG)

_______________________________

### 6. Easy Ensemble

* The accuracy score of 0.915.
* Overall precision score is 0.99.
* High risk has extremely low precision of 0.05 (the highest out of all models, but we still cannot rely on its results in this particular case.
* Low risk has a high precision level of 1.0.
* About 90% (15394) of low risk instances would be predicted true positive.

***Confusion Matrix***

* Out of the 101 high risk instances (first row), the classifier predicted correctly 94 of them.
* Out of the 17104 low risk instances (second row), the classifier predicted correctly 15398 of them
* Out of sample of 17205, the classifier predicted correctly about 15492 of them. 


![](https://github.com/jojobear2020/Credit_Risk_Analysis/blob/main/images/easy_ensemble_adaboost_classifier_all.PNG)

_________________________

## Summary

Recommendation -  use accuracy only if the classes are perfectly balanced, and otherwise use F1 and MCC. It is also useful to see ratio of positives and negative estimation via precision and recall.

