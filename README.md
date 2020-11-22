# Credit_Risk_Analysis

## Analysis Purpose

TBU

## Analysis approach: 




## Important Metrics 

1.	**pre** – precision, which is a measure of result relevancy;
2.	**rec** – recall, which is the same as sensitivity. Recall is a measure of how many truly relevant results are returned;
3.	**spe** – specificity;
4.	**f1** – harmonic average of the precision and recall; 
5.	**geo** – geometric mean of specificity and sensitivity;
6.	**iba** – index of imbalanced accuracy.


**When we have imballanced data (like in our case), F1 metric is the best to use. Simply stated the F1 score sort of maintains a balance between the precision and recall for the classifier. If precision is low, the F1 is low, and if the recall is low again, the F1 score is low**.


![](https://github.com/jojobear2020/Credit_Risk_Analysis/blob/main/images/f1_formula.PNG)

_____________________________________

## Machine Learning Models

### 1. Naive Random Oversampling

* The accuracy score of **0.650** is quite low.
* Overall precision score is 0.99.
* Recall/sensitivity score is 0.61.
* **F1 score is 0.75**.


***Confusion Matrix***

* Out of the 101 instances (first row), the classifier predicted correctly 70 of them (true positive).
* Out of the 17104 instances (second row), the classifier predicted correctly 10393 of them (true negative).
* Out of sample of 17205, the classifier predicted correctly/true about 10463 (61%) of them (see rec score); 6742 (39%) were false/inaccurate predictions.


![]( https://github.com/jojobear2020/Credit_Risk_Analysis/blob/main/images/naive_random_oversampling_all.PNG)

____________________________


### 2. SMOTE Oversampling

* The accuracy score of **0.662** is quite low.
* Overall precision score is 0.99.
* Recall/sensitivity score is 0.69.
* **F1 score is 0.81**


***Confusion Matrix***

* Out of the 101 instances (first row), the classifier predicted correctly 64 of them (true positive).
* Out of the 17104 instances (second row), the classifier predicted correctly 11813 of them (ture negative).
* Out of sample of 17205, the classifier predicted correctly/true about 11877 (69%) of them; 5328 (31%) were false/inaccurate predictions

![]( https://github.com/jojobear2020/Credit_Risk_Analysis/blob/main/images/smote_oversampling_all.PNG)

__________________________

### 3. Undersampling

* The accuracy score of **0.662** is quite low (neary identical to SMOTE).
* Overall precision score is 0.99.
* Recall/sensitivity score is 0.42.
* **F1 score is 0.58**


***Confusion Matrix***

* Out of the 101 instances (first row), the classifier predicted correctly 68 of them (true positive).
* Out of the 17104 instances (second row), the classifier predicted correctly 7100 of them (true negative).
* Out of sample of 17205, the classifier predicted correctly/true about 7168 (42%) of them; 10037 (58%) were false/inaccurate predictions.



![]( https://github.com/jojobear2020/Credit_Risk_Analysis/blob/main/images/undersampling_all.PNG)

_____________________________

### 4. SMOTEENN

* The accuracy score of **0.544** is very low (lowest by far).
* Overall precision score is 0.99.
* Recall/sensitivity score is 0.57.
* **F1 score is 0.72**


***Confusion Matrix***

* Out of the 101 instances (first row), the classifier predicted correctly 79 of them (true positive).
* Out of the 17104 instances (second row), the classifier predicted correctly 9795 of them (true negative).
* Out of sample of 17205, the classifier predicted correctly/true about 9874 (57%) of them; 7331 (43%) were false/inaccurate predictions.

![]( https://github.com/jojobear2020/Credit_Risk_Analysis/blob/main/images/smoteenn_all.PNG)

______________________

### 5. Balanced Random Forest Classifier

* The accuracy score of **0.788**.
* Overall precision score is 0.99.
* Recall/sensitivity score is 0.87.
* **F1 score is 0.93**


***Confusion Matrix***

* Out of the 101 instances (first row), the classifier predicted correctly 71 of them (true positive).
* Out of the 17104 instances (second row), the classifier predicted correctly 14951 of them (true negative).
* Out of sample of 17205, the classifier predicted correctly/true about 15022 (87%) of them;  2183 (13%) were false/inaccurate predictions.



![](https://github.com/jojobear2020/Credit_Risk_Analysis/blob/main/images/balanced_random_forester_classifier_all.PNG)

_______________________________

### 6. Easy Ensemble

* The accuracy score of **0.915**.
* Overall precision score is 0.99.
* Recall/sensitivity score is 0.90.
* **F1 score is 0.94** - the highest out of all models


***Confusion Matrix***

* Out of the 101 instances (first row), the classifier predicted correctly 94 of them (true posotive).
* Out of the 17104 instances (second row), the classifier predicted correctly 15398 of them (true negative).
* Out of sample of 17205, the classifier predicted correctly/true about 15492 (90%) of them;  1713 (10%) were false/inaccurate predictions.


![](https://github.com/jojobear2020/Credit_Risk_Analysis/blob/main/images/easy_ensemble_adaboost_classifier_all.PNG)

_________________________

## Summary

The summary below shows the key metrics reviewed in this analysis.  If our data was balanced, we could use accuarcy as our main KPI; however, we have a very imbalanced model and it's better to use F1. 

![](https://github.com/jojobear2020/Credit_Risk_Analysis/blob/main/images/summary_stats_all_models_details.PNG)

From our results, the most accuarate model is the last one - ***Easy Ensemble AdaBooster Classifier***. 

***Balanced Random Forest Classifier*** also delivers acceptable results; however, it is not as high. 

Based on this analysis, we can recommned to use these two models.

It is important to note is that there is no one size fits all when working with imbalanced datasets. A **suggestion** would be to actually try using all of the above approaches and see whatever works best in each particular case.


