
# Project: Predicting the status of "COVID-19" patients using Random Forests.

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

