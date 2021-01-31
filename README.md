# Random Forests

![RF](https://user-images.githubusercontent.com/67468718/106378751-fb0c6780-635b-11eb-8b2b-ec0662a35f9e.JPG)

## Introduction:

**Random Forest** is an ensemble of Decision Trees. With a few exceptions. A RandomForestClassifier has all the hyperparameters of:
  * **DecisionTreeClassifier** (to control how trees are grown).
  * **BaggingClassifier** to control the ensemble itself.

The Random Forest algorithm introduces extra randomness when growing trees; instead of searching for the very best feature when splitting a node, it searches for the best feature among a random subset of features. This results in a greater tree diversity, which (once again) trades a higher bias for a lower variance, generally yielding an overall better model. 

