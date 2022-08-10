# Project Name
- Advanced Regression Assignment - Surprise Housing


## Table of Contents
* [General Info](#general-information)
* [Business Objectives](#business-objectives)
* [Methodology Used](#methodology-used)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
A US-based housing company named Surprise Housing has decided to enter the Australian market. The company uses data analytics to purchase houses at a price below their actual values and flip them on at a higher price. For the same purpose, the company has collected a data set from the sale of houses in Australia. The data is provided in the CSV file below. 

The company is looking at prospective properties to buy to enter the market. You are required to build a regression model using regularisation in order to predict the actual value of the prospective properties and decide whether to invest in them or not. 

The company wants to know:

1. Which variables are significant in predicting the price of a house, and

2. How well those variables describe the price of a house.

 
Also, determine the optimal value of lambda for ridge and lasso regression.

 
Business Goal 

 
You are required to model the price of houses with the available independent variables. This model will then be used by the management to understand how exactly the prices vary with the variables. They can accordingly manipulate the strategy of the firm and concentrate on areas that will yield high returns. Further, the model will be a good way for management to understand the pricing dynamics of a new market.

Dataset used

- day.csv - https://ml-course3-upgrad.s3.amazonaws.com/Assignment_+Advanced+Regression/train.csv
- Data dictionary - https://cdn.upgrad.com/UpGrad/temp/87f67e28-c47e-4725-ae3c-111142c7eaba/data_description.txt

## Business Objectives
The company wants to know:

- Which variables are significant in predicting the price of a house
- How well those variables describe the price of a house

We are required to model the price of houses with the available independent variables. This model will then be used by the management to understand how exactly the prices vary with the variables. They can accordingly manipulate the strategy of the firm and concentrate on areas that will yield high returns. Further, the model will be a good way for management to understand the pricing dynamics of a new market.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->
## Methodology Used (High level steps)
- First step we imported the dataset, understood and visualized the dataset for basic information
- Next we did and Exploratory data analysis on the dataset to clean the dataset and prepare the dataset for modelling. 
       - Missing value imputation
       - Data type correction, assigning correct datatype
       - Outlier treatment
       - Derived columns
       - Removing unnecessary features based on the EDA

- Built a basic linear regression model and RFE model to see if it works, but both had some shortcomings i.e. overfitting and low model accuracy. 
- To overcome that we moved to Ridge and Lasso regularization techniques to build the models using the features we arrived at after the EDA. 
- After that we did residual analysis, prediction on the test data and model evaluation. 
- We also created the Ridge and Lasso regularization models with all the features to see if that improves the accuracy and errors
       - For this we just applied data pre-processing to the dataset and applied the Ridge and Lasso regularization
- We also created a view to compare the outputs and metrices from different models in a table
- We identified the most important features impacting the target variable. 
- Made some changes to models to answer the subjective questions in the second part of this assignment
- Finally concluded with the summary. 
<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- IDE - Jupyter notebook
- Language - Python 3.0
- libraries
    - Pandas
    - Numpy
    - Matplotlib
    - Seaborn
    - Statsmodels
    - Sklearn
        - LinearRegression
        - Ridge
        - Lasso
        - RFE
        - GridSearchCV etc.

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Conclusions
- Top 10 features that impact the house prices 
- Ridge Top 10 Features for Ridge with all features (alpha = 3)

       - 'GrLivArea', --->Above grade (ground) living area square feet
       - 'OverallQual_10',---> Rates the overall material and finish of the house, rating is 10 or not?
       - '1stFlrSF'--> First Floor square feet
       - 'BsmtFinSF1', ---> Type 1 finished square feet
       - 'TotalBsmtSF' --->Total square feet of basement area
       - '2ndFlrSF' ---> Second floor square feet
       - 'Neighborhood_StoneBr', --->Neighborhood is Stone Brook or not?
       - 'PoolQC_NoPool' ---> If the NoPool is Yes or no? It is negatively correlated i.e. price will be high if a pool is present in the property.
       - 'LotArea' ---> Lot size in square feet
       - 'FullBath_3', ---> Number of full bathrooms are 3 or not

- Top 10 Features for Lasso with all features(alpha = 0.0001)

       - 'GrLivArea', --->Above grade (ground) living area square feet
       - 'OverallQual_10',---> Rates the overall material and finish of the house, rating is 10 or not?
       - 'TotalBsmtSF' ---> Total square feet of basement area
       - 'OverallQual_9', ---> Rates the overall material and finish of the house, rating is 9 or not?
       - 'PropertyAge', --->Age of the property, it is negatively correlated.
       - 'BsmtFinSF1', --->Type 1 finished square feet
       - 'PropertyAge', --->Age of the property, it is negatively correlated.
       - 'PoolQC_NoPool' ---> If the NoPool is Yes or no? It is negatively correlated i.e. price will be high if a pool is present in the property.
       - 'Neighborhood_StoneBr', --->Neighborhood is Stone Brook or not?
       - 'Neighborhood_Crawfor' --->Neighborhood is Crawfor or not?
       - 'OverallQual_8', ---> Rates the overall material and finish of the house, rating is 8 or not?

We could see that more or less the final models predict almost same top 10 variables. However Lasso gives us an opportunity to reduce the 
number of predictors in the final model by changing the lambda, so we suggest to use Lasso regularization in this case as the number of predictor variables is very high in this case. 

## Acknowledgements
Give credit here.
- This project was inspired by the knowledge and learning provided to us during our live sessions and couse provied by UpGrad and IIIT(Bangalore)


## Contact
Created by [@gautamjoshi1984] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
