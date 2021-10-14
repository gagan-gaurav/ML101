---
description: >-
  Various Types of evaluation metrics for Different use cases of Machine
  Learning.
---

# Evaluation Metrics

![Most Useful Metrics](<.gitbook/assets/image (17).png>)

### Regression Metrics 

#### 1. RMSE

It represents the [sample standard deviation](https://en.wikipedia.org/wiki/Sample_standard_deviation) of the differences between predicted values and observed values (called residuals). Mathematically, it is calculated using this formula:

\


![](<.gitbook/assets/image (18).png>)

#### 2. MAE 

The MAE is a linear score which means that all the individual differences are weighted equally in the average.

![](<.gitbook/assets/image (19).png>)

#### Which One to Use accordingly? 

It is easy to understand and interpret MAE because it directly takes the average of offsets whereas RMSE penalizes the higher difference more than MAE.

Even after being more complex and biased towards higher deviation, RMSE is still the default metric of many models because the loss function defined in terms of RMSE is smoothly differentiable and makes it easier to perform mathematical operations.

#### R Squared and Adjusted R-Squared 

R Squared & Adjusted R Squared are often used for explanatory purposes and explains how well your selected independent variable(s) explain the variability in your dependent variable(s)

![R Squared](<.gitbook/assets/image (20).png>)

The Numerator is MSE and the denominator is variance, Higher the MSE less is the R-square. 

Adjusted R-Squared: Just like R², adjusted R² also shows how well terms fit a curve or line but adjusts for the number of terms in a model

![Adjusted R Squared](<.gitbook/assets/image (21).png>)

An adjusted R² will consider the marginal improvement added by an additional term in your model. So it will increase if you add useful terms and it will decrease if you add less useful predictors. However, R² increases with increasing terms even though the model is not actually improving. 

### Classification Metrics

![](<.gitbook/assets/image (22).png>)



* **Recall or Sensitivity or TPR (True Positive Rate)**: Number of items correctly identified as positive out of total true positives- TP/(TP+FN)
* **Specificity or TNR (True Negative Rate): **Number of items correctly identified as negative out of total negatives- TN/(TN+FP)
* **Precision:** Number of items correctly identified as positive out of total items identified as positive- TP/(TP+FP)
* **False Positive Rate or Type I Error:** Number of items wrongly identified as positive out of total true negatives- FP/(FP+TN)
* **False Negative Rate or Type II Error:** Number of items wrongly identified as negative out of total true positives- FN/(FN+TP)
* **Confusion Matrix: **

![Confusion Matrix](<.gitbook/assets/image (23).png>)

* **F1 Score**: It is a harmonic mean of precision and recall given by-\
  F1 = 2\*Precision\*Recall/(Precision + Recall)
* **Accuracy:** Percentage of total items classified correctly- (TP+TN)/(N+P)

#### ROC-AUC Curve

 A **ROC curve** (**receiver operating characteristic curve**) is a graph showing the performance of a classification model at all classification thresholds. This curve plots two parameters:

* True Positive Rate
* False Positive Rate

 **AUC** stands for "Area under the ROC Curve." That is, AUC measures the entire two-dimensional area underneath the entire ROC curve (think integral calculus) from (0,0) to (1,1).

![ROC-AUC Curve](<.gitbook/assets/image (24).png>)

* ROC-AUC score is independent of the threshold set for classification because it only considers the rank of each prediction and not its absolute value. The same is not true for the F1 score which needs a threshold value in the case of probabilities output.



