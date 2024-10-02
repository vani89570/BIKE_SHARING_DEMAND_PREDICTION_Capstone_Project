# **Seoul Bike Sharing Demand Prediction**



##### **Project Type**    - Regression
##### **Contribution**    - Individual
##### **A Project By**    - Vani Bhatt



from google.colab import drive
drive.mount('/content/drive')

# **Project Summary -**

This project aims to enhance the mobility and convenience of the public through bike-sharing programs in metropolitan areas. One of the main challenges is maintaining a consistent supply of bikes for rental. Bike-sharing systems are automated and enable people to rent and return bikes at various locations. The project focuses on utilizing historical data on factors such as temperature and time to predict the demand for the bike-sharing program in Seoul.


* There were approximately 8760 records and 14 attributes in the dataset.
* We started by importing the dataset, and necessary libraries and conducted exploratory data analysis (EDA).
* There were no Outliers and null values found in the dataset.Created new variables such as weekend_weekdays, Data were transformed to ensure that it was compatible with machine learning models.
* We handled target class imbalance using square root normalization.
* Then finally cleaned and scaled data was sent to 10 various models, the metrics were made to evaluate the model, and we tuned the hyperparameters to make sure the right parameters were being passed to the model.
* When developing a machine learning model, it is generally recommended to track multiple metrics because each one highlights distinct aspects of model performance. We are, focusing more on the R2 score and RMSE score.
*  The R2 score is scale-independent, which means that it can be used to compare models that are fit to different target variables or to target variables that have different units of measurement. This is particularly useful when comparing models for different problems, as it allows for a direct comparison of the performance of the models, regardless of the scale of the target variable

# **Index**

1.   Problem Statement
2.   Know Your Data
3.   Understanding Your Variables
4.   EDA
5.   Data Cleaning
6.   Feature Engineering
7.   Model Building
8.   Model Implementaion.
9.   Conclusion

# **Problem Statement**
Currently Rental bikes are introduced in many urban cities for the enhancement of mobility comfort. It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, proving a city with a stable supply of rental bikes becomes a major concern. The crucial part is the prediction of bike count required at each hour for the stable supply of rental bikes.

**Data Description**

**Fields : Description**

Date : Date/month/year

Rented Bike Count : Count of rented bikes per hour

Hour : Hour of the day

Tempareture : Temparature of the day

Humidity : Humidity measure

Windspeed : Windspeed(m/s)

Visibility : Visibility Measure (10m)

Dew Point Tempareture : Dew Point Tempareture Measure

Solar Radiation : Solar Radiation measure

Rainfall : Rainfall in mm

Snowfall : Snowfall measure (cm)

Seasons : 1=spring, 2=summer, 3=fall, 4=winter

Holiday : Whether a holiday or not

Functional Day : Whether a functional or not

# WorkFlow

# Data Wrangling

  No duplct values
  No Nan values & visualisation of null values in dataset
  Date column to day, month,year and save day col 0,1 by weekday n weekend col n drop date,day, year
  N unique values in each col
  Changing dtype int of cols hour,month,weekdays_weekend to category

# Data Vizualization

- Month
  Count of Rented bikes according to Month

- weekdays_weekend
  Count of rented bikes according to weekdays (0) and weekends (1)

- Hour
  Hourly Count of rented bikes according to weekdays and weekends

  Count of Rented bikes according to Hour

- Functioning Day
  Barplt -Count of Rented bikes according to wheather it is a Functioning Day or not

  Pointplt -Hourly Count of Rented bikes according to wheather it is a Functioning Day or not

- Seasons
  Barplt-Count of Rented bikes according to Seasons
  Displt-Count of Rented bikes according to Seasons
  Hourly Count of Rented bikes according to seasons

- Holiday
  - Count of Rented bikes according to Holiday

  - Hourly Count of Rented bikes according to Holiday

# Feature Engineering & Data Pre-processing
-  Analysis of Numerical variable of dtype int,flot

Analysis of data distribution of each numerical feature
-Numerical vs Rented_Bike_Count

- Analysing the relationship between
  'Rented_Bike_Count' and 'Temperature'
  'Rented_Bike_Count' and 'Solar_Radiation'
  'Rented_Bike_Count' and 'Snowfall'
  'Rented_Bike_Count' and 'Rainfall'
  'Rented_Bike_Count' and 'Wind_speed'

- Pair plot for the Count of Rented bikes according to Hour  & month

- Regression plot
  Visualising the regression plot for all the numerical features

- Normalise Rented_Bike_Count column data
  Data Distribution plot of Rented Bike Count with mean, median

# Handling Outliers
## Boxlpot for dependent variable Rented Bike Count to check outliers

- Applying square root to Rented Bike Count to improve skewness

- Boxplt- After applying sqrt on Rented Bike Count check wheather we still have outliers

-Checking of Correlation between variables
  Checking in OLS Model
  Fit ols model and check summary

- Chart - Correlation Heatmap

- Create the dummy variables for categorical columns
 - Assign all categorical features to a variable
- Copying df before Categorical Encoding - one hot encoding

- Data Splitting
  Model Training
  Train Test split for regression

- Data Scaling
- Data Transformation using minmax scaler

# ML Model Implementation using 
- LINEAR REGRESSION, RIDGE REGRESSION,  ELASTIC NET REGRESSION, KNeighbors Regressor,Support Vector Regressor,

## Predict on model
- visualisation of actual and predicted values
  - best fit line on test data
  - comparing act n pred test data on last 20 points
  - Cross- Validation Score

-Decision Tree Regressor,
Random Forest Regressor,
  Hyperparameter tuning-
  GridSearchCV - predict, Cross- Validation Score,Model Explainability

-Decision Tree Regressor,
  AdaBoost
  predict,Cross- Validation Score, Model Explainability

- Xtreme Gradient Boosting,Light GBM
  Hyperparameter tuning-
  GridSearchCV - predict, Cross- Validation Score,Model Explainability

- Comparing Performance of all the models and choosing final model with best performance



