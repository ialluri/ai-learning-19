## About

This study considers real data collected from a Portuguese retail bank, between May 2008 and November 2010 with 11.2% of success. The objective of this excercise is develop a model to predict if a contact is likely to subscribe to a term deposit.

The data comes from direct marketing performed by a bank.

The dataset collected is related to 17 campaigns

## Approach

The goal is to build a prective model that can label a data items into either "yes" or "no".

We are using bank information features (the first 7 columns).

1. We split the data with 60% for training and 40% for testing.

2. Build a baseline model.

![baseline model](image.png)

SVM Model is the slowest for training the data.

But the given the accuracy level of Training Data and although it is a bit slower than KNN the inclination is to use Decision Tree.

But I must admit even KNN algorithm is pretty good start.

3. Finally performed cross validation with grid search to find the best estimator for Decision Tree. It turns out the max_depth=5 yields best result.

```
 DecisionTreeClassifier(criterion='entropy', max_depth=5, min_samples_leaf=50,
                       random_state=42)
```

Which again comes closer to knn.
