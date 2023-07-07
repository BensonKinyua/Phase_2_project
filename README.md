# Phase_2_project
# House Price Prediction Analysis for Real Estate Agents In NorthWestern County
A well executed sample project, that uses multiple linear regression and python code to show how to predict house prices in NorthWestern County.
# Project overview
This is a project that focuses on analyzing the King County House Sales dataset. The goal of using this data is to find correlating factors with the price of a house so that I can make recommendations to the real-estate company based on the findings. Looking for factors that contribute a large amount to the variation of the price of a home so that better business recommendations can be made based on those factors.

## Business Problem
Our stakeholder is a real-estate company who are looking to expand to NorthWestern County. They need a reliable metric for house prices and would like to know which features of houses are more impactful on the price. My task is to provide them with a multiple linear regression model that will provide them with an equation which will include features that are most important in determining housing prices. By applying multi linear regression  and analyzing the King County housing dataset, I aim to uncover the significant factors that drive house prices. This analysis will enable real estate agents to navigate the local market and provide accurate pricing recommendations.

## Data
This project uses 2014-2015 data from the King County House Sales dataset. It includes information on over 21,500 houses describing features such as year of renovation,space,number of bedrooms condition, etc

## Data Understanding
For this project, I will be using the King County House Sales dataset, the dataset includes various features such as the price, number of bedrooms,number of bathrooms, living area size, house grade, condition of the house, just to name a few.

The dataset has 21 columns and over 21597 rows, covering sales of houses between the years 2014 and 2015. 

The King County House Sales dataset contains the following columns:

* `id` - Unique identifier for a house
* `date` - Date house was sold
* `price` - Sale price (prediction target)
* `bedrooms` - Number of bedrooms
* `bathrooms` - Number of bathrooms
* `sqft_living` - Square footage of living space in the home
* `sqft_lot` - Square footage of the lot
* `floors` - Number of floors (levels) in house
* `waterfront` - Whether the house is on a waterfront
* `view` - Quality of view from house
* `condition` - How good the overall condition of the house is. Related to maintenance of house.
* `grade` - Overall grade of the house. Related to the construction and design of the house.
* `sqft_above` - Square footage of house apart from basement
* `sqft_basement` - Square footage of the basement
* `yr_built` - Year when house was built
* `yr_renovated` - Year when house was renovated
* `zipcode` - ZIP Code used by the United States Postal Service
* `lat` - Latitude coordinate
* `long` - Longitude coordinate
* `sqft_living15` - The square footage of interior housing living space for the nearest 15 neighbors
* `sqft_lot15` - The square footage of the land lots of the nearest 15 neighbors

The analysis performed on the dataset included the following steps:

1. Data Cleaning: Rows with missing data were dropped, and duplicate entries were removed.

2. Data Transformation: Categorical data in the `view`, `date`, `grade`, `condition` and `waterfront` columns were converted into numerical data using label encoding.

3. Exploratory Data Analysis: Various checks were conducted to assess the linearity assumptions between the target and predictor variables and identify any potential multicollinearity issues.

## Modeling
The final model took four factors in the end, Square Footage, Square footage of living15, Grade and number of bedrooms. I chose these factors based on their correlation with the target factor, the house price. I checked the colinearity on all the factors and even through some factors out of the model based on their high collinearity with Square Footage.  My R-squared Value was 54.1%, meaning that with the model can be able to explain 54.1% of the variation in a home's price. The mean squared error for the model was also significantly smaller than the baseline model and significantly smaller than all the other models. Each variable in the model also has a significant P value. 

## Results of the Modelling
The final model has a r-squared score of 0.537, meaning that 54% of the variance in the dataset is described by the model.
The final model had a Mean Absolute Error of 163,441 and Root Mean Squared Error of 245,084. This is low compared to the other two models. 
The model features had a p-value < 0.05 (our alpha/significance level), which tells us that all features have a statistically significant linear relationship with price.
The final model included 5 of the most significant predictor variables of house price. They are, Intercept, grade, sqft_living, sqft_living15 and bathroom.
The final model3 when compared to the baseline model, the R-squared increase from 49.6% to 54%

## Recommendations
* In NorthWestern County, square footage, square foot living, grade, and bathrooms have been identified as the most important factors in determining the price of house. When increasing the square footage and improving the grade of the house the home sellers should  also consider adding more bathrooms since from the analysis there exists positive relationship between these four factors.

* The real estate market is a industry that is dynamic and constantly changes. To ensure the model validity and continuous accuracy, the models needs to be regularly retrained using the latest data. This will help capture any shifts or trends in the market and maintain the model's effectiveness.

## Conclusions

* The more the number of bathrooms, the more expensive the house.

* The better the grade of the house, the more expensive the house.

* Square Footage of Living Space: The square footage of living space has a positive impact on house prices. As the size of the living space increases, the estimated price of the house also increases. This indicates that larger houses are generally priced higher.

* The model provides valuable insights into the factors affecting house prices in NorthWestern County and offers recommendations for homeowners and researchers interested in understanding the housing market dynamics.

* The selected features in our model were statistically significant linear relationships with the price, since their p-values was less than the alpha, thus the assumptions of independence, linearity, and normality were met.

# Required installations

This project requires Python 3.10 and the following Python libraries installed:

Numpy

Pandas

matplotlib

scikit-learn

scipy

Seaborn

statsmodels

The link to non-technical presentation: https://www.canva.com/design/DAFn7io73Co/4k0I6s7PYLxtL8DzkEsOpQ/edit.