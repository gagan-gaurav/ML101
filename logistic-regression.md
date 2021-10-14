# Logistic Regression

It is called logistic regression because it performs regression on [logits](https://en.wikipedia.org/wiki/Logit), which then allows us to classify the data based on model probability predictions.

For the math, head over to this [link](https://www.analyticsvidhya.com/blog/2021/07/an-introduction-to-logistic-regression/).

Also, Read this [Link](https://www.ritchieng.com/logistic-regression/) for Advanced Grasp on Logistic Regression.

![Five types of Solvers in Logistic Regression](<.gitbook/assets/image (7).png>)

![Cost Function in Logistic Regression](<.gitbook/assets/image (9).png>)

Check out the Scratch Implementation [here](https://github.com/RheagalFire/Scratch-Implementations/blob/master/Logistic%20Regression.ipynb).

### ** What Are the Basic Assumption?**

1. Linear Relation between independent features and the log-odds.

### Advantages 

1. Logistic Regression is very easy to understand.
2. It requires less training.
3. Good accuracy for many simple data sets and it performs well when the dataset is linearly separable.
4. It makes no assumptions about distributions of classes in feature space.
5. Logistic regression is less inclined to over-fitting but it can overfit in high dimensional datasets. One may consider Regularization (L1 and L2) techniques to avoid over-fitting these scenarios.
6. Logistic regression is easier to implement, interpret, and very efficient to train.

### Disadvantages

1. Sometimes Lot of Feature Engineering Is required
2. If the independent features are correlated it may affect performance
3. It is often quite prone to noise and overfitting
4. If the number of observations is lesser than the number of features, Logistic Regression should not be used, otherwise, it may lead to overfitting.
5. Non-linear problems can’t be solved with logistic regression because it has a linear decision surface. Linearly separable data is rarely found in real-world scenarios.
6. It is tough to obtain complex relationships using logistic regression. More powerful and compact algorithms such as Neural Networks can easily outperform this algorithm.
7. In Linear Regression independent and dependent variables are related linearly. But Logistic Regression needs that independent variables are linearly related to the log odds (log(p/(1-p)).
8. Sensitive to missing values and outliers.

