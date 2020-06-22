# NYC Airbnb Price Prediction 
04/20-06/20

### Introduction 

This project uses exploratory data analysis techiques to understand Airbnb data in NYC. I then use a variety of machine learning models to predict rental prices based on characteristics such as location, size, and description.

### Data 

The csv file used for the analysis can be found in the "data" folder in this repository.

The data comes from Kaggle. Please see [here](https://www.kaggle.com/dgomonov/new-york-city-airbnb-open-data)

### Notebooks 

This repository contains two notebooks: "NYC Airbnb Prediction- Low Prices" and "NYC Airbnb Prediction- Whole Price Range". The data cleaning, EDA, and modelling steps are largely the same in both; however, the Low Price notebook only includes listings in the dataset below $250, effectively dropping the top 10% of the target. 

There is also a directory called "models" which contains the pkl files for the KNN regressor models, as running these models takes a long time. By cloning the repository, users will not have to re-run the models on their own machines.

### Libraries

- numpy
- pandas
- sklearn
- keras
- matplotlib
- seaborn
- plotly
- scipy
- statsmodels
- wordcloud



### Modelling

This project uses a variety of modelling techniques including:<br>

- Linear Regression
- Lasso Regression
- Logistic Regression 
    - on count vectorized "name" column to understand which words are most predictive of price
- Ridge Regression 
- Decision Tree Regressor
- Random Forest Regressor
-Gradient Boosting Regressor
- KNN Regressor
- Neural Network



### Results 
Due to the high skew in the price distribution, the models performed significantly better on the low price data than on the entire dataset. The best model in the low price data results in an RMSE of 32, while the best performing model for the entire dataset results in an RMSE of ____________. 

The Random Forest Regressor performs the best on the low prices data. 

### Future Steps
The main area this project falls short in is accuracy on high price data. The main features that are missing are square footage, number of bedrooms, and amenities. Based on some quick research, a lot of the higher priced units are quite large, have many beds available, and many amenities. 

It would be interesting to see if photo data could contribute to the accuracy, since a lot of the listings that are a few thousand dollars a night tend to have extremely nice interior design. The dataset used for modelling in this project might not be capturing the general "niceness" of an apartment to the same degree that photo data would be able to. 

Overall, further data collection and feature engineering might be needed to accurately predict the top of the Airbnb market in NYC. 


