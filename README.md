**Multiple Linear Regression Predictive Modeling for House Prices in King County**

by Sam Odongo

**Presentation [here](https://docs.google.com/presentation/d/1zL_GFJgm1-n6oTwkgmK1RTXUnCPFPeDDRoDbj6gbEj4/edit#slide=id.gc6f980f91_0_0)**


![image]([https://github.com/sogodongo/Phase-1-Project/assets/103502854/940eb443-2445-4739-9395-bcd21f4d33f3](https://github.com/sogodongo/King-County-House/blob/master/KC%20Housing%20Image.jpg)https://github.com/sogodongo/King-County-House/blob/master/KC%20Housing%20Image.jpg)



# 1. Business Understanding
##  a) Introduction


The real estate market in King County is dynamic, and accurately predicting house prices is essential for informed decision-making by buyers and sellers. This project aims to develop a predictive model that can estimate house prices based on various features in the King County House Sales dataset. By leveraging data visualization techniques and conducting comprehensive analysis, we can gain valuable insights into the factors that significantly impact house prices. The objective is to build a robust regression model that effectively captures these relationships and provides accurate predictions. Additionally, by utilizing visualization and analysis, we can enhance our understanding of the dataset, facilitate model interpretation, and provide actionable recommendations to homeowners based on the model's insights.


## b) Problem Statement

The main problem addressed in this project is the lack of an efficient method to predict house prices accurately in King County. Existing methods might not consider all relevant features and may lead to inaccurate estimations. This project aims to develop a predictive model that takes into account multiple variables and accurately predicts house prices in King County.

## c) Main Objective:
The main objective of this project is to develop an accurate predictive model that can estimate house prices in King County based on various features. By analyzing the King County House Sales dataset and implementing appropriate multiple regression model, the goal is to create a reliable tool for buyers, sellers, and real estate professionals to make informed decisions about house prices in the region.


## d) Specific Objectives:

1. Develop and evaluate multiple linear regression model to identify the most influential factors that impact house prices in the King County housing market. This will involve exploring various regression algorithms and feature selection techniques to determine the key predictors of house prices.

2. Assess the performance of the developed  model in predicting house prices.Evaluate the model based on relevant metrics such as mean absolute error (MAE), root mean square error (RMSE), and R-squared to measure their accuracy and effectiveness in predicting future house prices.

   
## e) Defining Metrics for Success

_Model Development_
Success will be achieved by identifying the most influential factors that impact house prices in the King County housing market. The model should effectively capture the relationships between the predictor variables (such as bedrooms, bathrooms, square footage, condition, etc.) and the target variable (house prices). This involves conducting thorough feature selection, considering variable interactions, and ensuring the model's interpretability.

_Predictive Performance_
Success will be measured by evaluating the model's predictive performance using various metrics. The key metrics include:

a) Mean Absolute Error (MAE): A successful model will have a low MAE, indicating that, on average, the predicted house prices are close to the actual prices.

b) Root Mean Square Error (RMSE): A successful model will have a low RMSE, which measures the average magnitude of the model's prediction errors.

c) R-squared (R^2): A successful model will have a high R-squared value, indicating a high percentage of variance explained by the model. This reflects the model's ability to capture the variation in house prices based on the selected features.

_Interpretability and Actionability_
The developed model should be interpretable and provide actionable insights. It should allow stakeholders to understand the impact of each predictor variable on house prices and make informed decisions based on the model's insights.

## e) Experimental Design

Data Understanding
Data Exploration and Preparation
Feature Selection
Modelling
Fitting the Model
Interpretation of Coefficients and Evaluation of Modet Fit
Model Validation
Interpret and Communicate Results and Recommendations



##  f) Data Understanding

The data used in this project,that has 20 columns and 21597 rows,was downloaded from [here](https://www.kaggle.com/datasets/harlfoxem/housesalesprediction)
, consists of information related to house sales. Here is a description for each column:


**id**: A unique identifier for each house.

**date**: The date when the house was sold.

**price**: The target variable representing the price of the house.

**bedrooms**: The number of bedrooms in the house.

**bathrooms**: The number of bathrooms in the house.

**sqft_living**: The square footage of the home.

**sqft_lot**: The square footage of the lot.

**floors**: The total number of floors in the house.

**waterfront**: Indicates whether the house has a view to a waterfront.

**view**: Indicates whether the house has been viewed.

**condition**: Represents the overall condition of the house.

**grade**: Represents the overall grade given to the housing unit based on the King County grading system.

**sqft_above**: The square footage of the house apart from the basement.

**sqft_basement**: The square footage of the basement.

**yr_built**: The year the house was built.

**yr_renovated**: The year when the house was renovated.

**zipcode**: The zip code of the house's location.

**lat**: The latitude coordinate of the house's location.

**long**: The longitude coordinate of the house's location.

**sqft_living15**: The square footage of interior housing living space for the nearest 15 neighbors.

**sqft_lot15**: The square footage of the land lots of the nearest 15 neighbors.


## 2.Exploratory Data Analysis

### a) Examining the Target Variable, 'Price'

 i) Examining the Correlation between Features and Price
ii) Examination of Association of Ordinal Features with the Target Variable, Price
iii) Examination of Association of Continuous Features with the Price¶
iv) Examination of Association of Waterfront feature with the Price

### b) Building a Mutiple Regression Model

  Feature Selection
   Assumption
   Multicollinearity
   Linear relationship between explanatory and response variables
   Homoscedasticity of error terms
   Normal distribution of model residuals
   Modelling
   
### c)Model Validation

### d)Interpretation of Model Results

## 3.Conclusions

_The multiple regression model demonstrates that approximately 53.4% of the variation in house prices can be explained by the included variables: the number of bathrooms, grade, square footage of living space, and square footage of the land lots of the nearest 15 neighbors (sqft_living15).

_The highly significant F-statistic of 6000 indicates that the overall model is statistically significant, signifying that the combined effects of the independent variables significantly contribute to predicting house prices.

_The coefficients offer valuable insights into the relationship between the independent variables and house prices:

_Each additional bathroom is associated with a decrease of $22,800 in house price, holding other factors constant

_A higher grade is linked to a higher house price, with each unit increase in grade leading to an increase of $187,900 in price.

_An increase in the square footage of living space is associated with a higher house price, with each unit increase resulting in an increase of $362,100 in price.

_More square footage of interior housing living space among the nearest 15 neighbors (sqft_living15) is connected to a higher house price, with each unit increase leading to an increase of $183,000 in price.

_The normality assumption of the model is satisfied based on the QQ-plot of the model residuals. Additionally, the scatter plot of residuals vs predicted values indicates that the residuals are centered around zero and exhibit random patterns, suggesting that the linear regression assumptions are reasonably met.

_The MSE values suggest that the multiple regression model is capturing some of the variation in the target variable, but there is still room for improvement. It's important to consider additional evaluation metrics and potentially explore other modeling approaches to further optimize the model's performance.

## 4.Recommenations

_To Consumers/Investors/_.

+ When evaluating house prices, consider the factors included in the multiple regression model: number of bathrooms, grade, square footage of living space, and square footage of the land lots of the nearest 15 neighbors (sqft_living15).

+ Pay attention to the quality and grade of a house, as higher grades are associated with higher prices. This information can be useful when comparing properties or making investment decisions.

+ Consider the impact of square footage of living space on house prices. A larger living space is associated with higher prices, so this factor should be taken into account when assessing property values.

+ While the model indicates that more bathrooms are associated with lower prices, it is important to consider other factors and individual preferences. Some buyers may value additional bathrooms, so it's essential to evaluate the overall appeal and functionality of a property.

_To Data Professionals_

+ The model assumes linearity and other assumptions of multiple regression. When making predictions or drawing conclusions, it is crucial to consider these assumptions and their potential limitations.

+ Regularly assess and validate the model's performance using metrics such as mean squared error. This will help gauge the accuracy and predictive power of the model and identify any potential areas for improvement.

+ Keep in mind that other factors beyond those included in the model may also influence house prices. Consider incorporating additional variables or exploring alternative models to capture a more comprehensive understanding of house price dynamics in the real estate domain.




