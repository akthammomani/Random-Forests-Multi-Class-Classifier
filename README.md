# Random Forests

![Capture_rf](https://user-images.githubusercontent.com/67468718/106399014-1498c800-63cb-11eb-8d32-ed42b8bcf569.JPG)

## Introduction:

**Random Forest** is an ensemble of Decision Trees. With a few exceptions. A RandomForestClassifier has all the hyperparameters of:
  * **DecisionTreeClassifier** (to control how trees are grown).
  * **BaggingClassifier** to control the ensemble itself.

The Random Forest algorithm introduces extra randomness when growing trees; instead of searching for the very best feature when splitting a node, it searches for the best feature among a random subset of features. This results in a greater tree diversity, which (once again) trades a higher bias for a lower variance, generally yielding an overall better model. 


## Further Diveristy with Random Forests:
  * Random Forests is an ensemble method that uses a decision tree as a base estimator. 
  * Each estimator is trained on a different bootstrap sample having the same size as the training set. 
  * RF introduces further randomization than bagging when training each of the base estimators. 
  * When each tree is trained, only d features can be sampled at each node without replacement, where d is a number smaller than the total number of features.


