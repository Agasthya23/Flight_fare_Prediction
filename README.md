# Flight_Fare_Prediction

## Table of Contents
  * [Overview](#overview)
  * [Codes and Resources Used](#Codes-and-Resources-Used)
  * [EDA](#EDA)
  * [Feature Selection](#Feature-Selection)
  * [Model Selection](#Model-Selection)
  * [Model Deployment](#Model-Deployment)
  * [Future Scope](#Future-Scope)
 
## Overview
* Built a Flight_Fare_Prediction app that predicts the flight fare tickets that is useful for users while booking flight tickets.
* Implemented Random forest regressor model to the data and hyper tuned using RandomSearchCV to produce the best result.

* Deployed using Flask API.
* Built Model on Amazon Sagemaker.


![Front end](https://imgur.com/N5PReqb.png)

## Codes and Resources Used

* Python Version: 3.6
* Packages: pandas, numpy, sklearn, matplotlib, seaborn, flask, json, pickle
* For Web Framework Requirements: pip install -r requirements.txt
* Dataset: https://www.kaggle.com/nikhilmittal/flight-fare-prediction-mh
* Flask Productionization: https://towardsdatascience.com/productionize-a-machine-learning-model-with-flask-and-heroku-8201260503d2

## EDA

* Created separate columns for Departure and Arrival Hour and Minute from Dep_time and Arrival Time
* Similarly, created separate columns Duration_Hour and Duration_Min from Duration_time
* Removed ambiguity by replacing Delhi to New_Delhi in Soure and destination column
* Handled Null values
* Implemented one hot encoding

## Feature Selection
* Dropped Route Column, as it is similar to Total_stops column
* Plotted heatmap and found all the other columns were important

## Model Selection
* Fitted the model and calculated MSE values

MSE of LogisticRegression : 4961.954329674016

MSE of Lasso :  3097.2118855308195


MSE of Ridge :  3053.511060846312


MSE of KNeighborsRegressor :  4888.9554779063865

 
MSE of DecisionTreeRegressor :  2136.604994752933


MSE of RandomForestRegressor :  1662.2005358843994


MSE of GradientBoostingRegressor :  2166.1071423971985

* RandomForest Regressor performed well with MSE value of 1662.20
* After Hyperparameter Tuning, MSE value decrease to 1662.20


## Model Deployment
* Built a  flask API endpoint that was hosted on a local webserver using Flask.
* After taking necessary input from the user returns the Flight Price.
* Also, built and deployed the model using Amazon Sagemaker

## Future Scope

* Use multiple Algorithms
* Optimize Flask app.py
* Front-End 






