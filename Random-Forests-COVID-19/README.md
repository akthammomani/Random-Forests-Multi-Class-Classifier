
# Project: Predicting COVID-19 Patients Status Using Random Forests Multi-Class Classifier.

![covidimage2](https://user-images.githubusercontent.com/67468718/106261986-2ca7f600-61d7-11eb-84e1-29362d5a425e.png)

## 1. Introduction: Coronavirus

Coronavirus disease (COVID-19) is an infectious disease caused by a new virus.
The disease causes respiratory illness (like the flu) with symptoms such as a cough, fever, and in more severe cases, difficulty breathing. You can protect yourself by washing your hands frequently, avoiding touching your face, and avoiding close contact (1 meter or 3 feet) with people who are unwell. An outbreak of COVID-19 started in December 2019 and at the time of the creation of this project was continuing to spread throughout the world. Many governments recommended only essential outings to public places and closed most business that do not serve food or sell essential items. An excellent [spatial dashboard](https://www.arcgis.com/apps/opsdashboard/index.html#/bda7594740fd40299423467b48e9ecf6) built by Johns Hopkins shows the daily confirmed cases by country. 

## 2. Objective

In this Project we'll be highlighting the important role that data science plays in real-world situations like this pandemic. So we'll be building **a Random Forest Classifier** to predict the 'state' of the patient.

## 3. Dataset
Using a dataset from the South Korean cases of COVID-19 provided on [Kaggle](https://www.kaggle.com/kimjihoo/coronavirusdataset) to encourage research on this important topic.

## 4. Sourcing and loading
- Import packages
- Load The Data
- Explore the data

## 5. Cleaning, Transforming, and Visualizing

- Check the intgerity of the data and let's try fix as much as possible if any.
- Handle Numerical Missing Data.
- Create a new column named 'n_age' which is the calculated age based on the birth year column.
- Drop Insignificant columns.
- Visualization
- Check for duplicated rows.
- Handle Categorical Missing Data Using **KNN imputer "fancyimpute"** to encode and impute the missing Data.
- Check for duplicated rows.

## 6. Random Forest Model
- Split the data into test and train subsamples
- Scale data to prep for model creation
- Fit Random Forest Classifier:
- Classification Report
- Create Confusion Matrix Plots
![cm](https://user-images.githubusercontent.com/67468718/106378205-cbf3f700-6357-11eb-8a1d-927fa2869c02.JPG)

## 7. Features Importance

![features_2nd_round](https://user-images.githubusercontent.com/67468718/106551781-d1be1980-64ca-11eb-9c2e-cab92d22e1d7.JPG)

## 8. Hyperparameter Tuning using GridSearchCV
| <code>Random Forests (Base)</code> | <code>Random Forests (Tuned)</code>|
|:---------------------:|:---------------------:|
|Accuracy= 85.360 %|Accuracy= 86.712 %|
|f1_score= 82.903 %|f1_score= 83.112 %|

## 9. Conclusion

 * The Random Forests (Base) Model shows an overall <code>accuracy of 85.36%</code>, which is great and indicates that our model was effectively able to identify the status of the COVID-19 patients in the South Korea dataset despite the fact that we have imbalanced class **"State"**, due to the nature of the dataset and the topic we're trying to tackle here which is **Predicting COVID-19 Patients State** , as shown below:

|<code>code</code>|<code>state</code>|<code>count</code>|
|:--:|:--: |:--:|
|1|isolated|    1878|
|2|released |    306|
|0|deceased |     34|

 * As shown in [The Decision Tree used in the Base Model](https://github.com/akthammomani/Random-Forests-Multi-Class-Classifier/blob/main/Random-Forests-COVID-19/DT_base.md) vs [the same Decision Tree used in the Tuned Model](https://github.com/akthammomani/Random-Forests-Multi-Class-Classifier/blob/main/Random-Forests-COVID-19/DT_Tuned.md), There's huge difference between the decision Tree we visualized using the Base Model compared to the Tuned Model. The Base Model lead to a fully grown and unpruned DT which looks very large. so after we fined tuned the Random Forest Parameters we managed to improve Accuracy by <code>1.3% from 85.36% to 86.712% </code>and there was a clear reduction in the Decision Trees size thus reducing memory consumption, the complexity and we find the split choices that will get us to the pure nodes much faster resulting in more information gain (more prediction power)
 * The popularity of random forest is primarily due to how well it performs in a multitude of data situations. It tends to handle highly correlated features well, where as a linear regression model would not. In this project we demonstrate the performance ability even with only a few features and almost all of them being highly correlated with each other.
Random Forest is also used as an efficient way to investigate the importance of a set of features with a large data set. Consider random forest to be one of your first choices when building a decision tree, especially for multiclass classifications.


