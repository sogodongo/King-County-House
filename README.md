# Multiple Linear Regression Predictive Modeling for House Prices in King County

by Sam Odongo

**Presentation [here](https://docs.google.com/presentation/d/1zL_GFJgm1-n6oTwkgmK1RTXUnCPFPeDDRoDbj6gbEj4/edit#slide=id.gc6f980f91_0_0)**


![image](https://github.com/sogodongo/King-County-House/blob/master/KC%20Housing%20Image.jpg)




# Overview

This project focuses on developing a multiple linear regression model for predicting house prices in King County. Accurate price estimation is crucial in the real estate market for both buyers and sellers to make informed decisions. By leveraging the King County House Sales dataset and employing data visualization and comprehensive analysis techniques, the project aims to identify the key factors that significantly impact house prices and build a reliable regression model.

The main objective is to develop a predictive model that accurately estimates house prices based on various features. The model will consider multiple variables and utilize regression algorithms and feature selection techniques to determine the most influential predictors of house prices in the King County housing market.

To assess the model's performance, relevant metrics such as mean absolute error (MAE), root mean square error (RMSE), and R-squared will be utilized. A successful model will demonstrate low MAE and RMSE values, indicating accurate predictions, and a high R-squared value, indicating a high percentage of variance explained by the model.

The project follows a structured experimental design that involves data understanding, exploration, and preparation. Feature selection techniques will be applied to identify the most relevant variables for the regression model. The model will be fitted, and the coefficients will be interpreted to evaluate the model's fit. Model validation will be performed to assess its predictive performance. Finally, the results and recommendations will be interpreted and communicated effectively to provide actionable insights to stakeholders in the real estate industry.

Thus,this project aims to provide a reliable and accurate predictive model for house prices in King County, enabling buyers, sellers, and real estate professionals to make informed decisions based on the model's insights and recommendations.



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

Here is a snippet of the data used:

![image](https://github.com/sogodongo/King-County-House/blob/master/Data%20Preview.png?raw=true)

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

### b) Building a Mutiple Linear Regression Model

 *Feature Selection*
  
   Assumptions
   
    + Multicollinearity
   
    + Linear relationship between explanatory and response variables
   
    + Homoscedasticity of error terms
   
    + Normal distribution of model residuals
   
      
Selected Feautures;For the Model I selected 4 feautures that had the highest correlation with price and did not violate the multocorrelianity assumption:

+ grade
+ bathrooms
+ sqft_living15
+ sqft_living

   
 *Modelling*
 
   *Methodology for Creating the Multiple Linear Regression Model*
    
    Created a new DataFrame with the selected variables:

     The variables 'bathrooms', 'grade', 'sqft_living', and 'sqft_living15' are chosen as the predictors for the regression model.
     A new DataFrame called 'df_selected' is created to store these selected variables.
     
     Updated the target variable and the sqft variables to their natural logarithm:

     The target variable 'price' is transformed using the natural logarithm.
     The variables 'sqft_living' and 'sqft_living15' are also transformed using the natural logarithm.
     Taking the logarithm can help to normalize the data and improve the model's performance.
     
    Performed ordinal encoding on the 'grade' column:

     The 'grade' column, which represents an ordinal feature, is encoded using the OrdinalEncoder.
     Ordinal encoding assigns a numerical value to each category based on its order or rank.
     
    Converted the data types of the columns to numeric:

     The data types of the columns 'bathrooms', 'grade', 'sqft_living', and 'sqft_living15' are converted to float to ensure consistency and ompatibility with the regression model.
     
    Added a constant column to the DataFrame:

    A constant column is added to the DataFrame using the sm.add_constant() function.
    This constant column represents the intercept term in the regression model.
    
    Fitting the multiple regression model:

    The multiple regression model was then fitted using the Ordinary Least Squares (OLS) method from the statsmodels library.
    The target variable 'price' was regressed on the other predictor variables in the DataFrame.
    The results of the regression model were then stored in the 'results' variable.
    
By following these steps, the code prepared the data and fitted a multiple regression model to predict house prices based on the selected variables. The regression results were further analyzed and interpreted to understand the relationships between the predictors and the target variable.


 *Model Results*

![image](https://github.com/sogodongo/King-County-House/blob/master/Model%20Results%20Image.png)
   
### c) Model Validation

 *MSE*
 
Train Mean Squared Error: 0.1222337541382977

Test Mean Squared Error: 0.1264896495280169

 *RMSE*
 
Train Root Mean Squared Error: 0.34961944187687516

Test Root Mean Squared Error: 0.35565383384411436


The low MSE and RMSE values denote the success of this model in predicting house prices
The difference between the two MSE/RMSE values is relatively small, indicating that the model's performance is consistent across both the training and testing sets.



### d) Interpretation of Model Results



+ The model has an R-squared value of 0.534, indicating that approximately 53.4% of the variation in house prices can be explained by the included variables: bathrooms, grade, square footage of living space, and square footage of interior housing living space for the nearest 15 neighbors(sqft_living15).

+ The highly significant F-statistic of 6000 suggests that the overall model is statistically significant, meaning that the combined effects of the independent variables significantly contribute to predicting house prices.

+ The intercept coefficient (const) is estimated to be 8.1050, indicating that when all other variables are zero, the average price of a house is estimated to be $8.1050 million.

+ The coefficient for the number of bathrooms (bathrooms) is -0.0228, indicating that, on average, each additional bathroom is associated with a decrease of $22,800 in house price, holding other factors constant.

+ The coefficient for the grade of the house (grade) is 0.1879, suggesting that a higher grade is associated with a higher house price. Each unit increase in grade leads to an increase of $187,900 in price.

+ The coefficient for the square footage of living space (sqft_living) is 0.3621, indicating that an increase in the square footage of living space is associated with a higher house price. Each unit increase in square footage leads to an increase of $362,100 in price.

+ The coefficient for the square footage of interior housing living space for the nearest 15 neighbors (sqft_living15) is 0.1830, suggesting that more living space among the nearest 15 neighbors is associated with a higher house price. Each unit increase in sqft_living15 leads to an increase of $183,000 in price.

+ The standard errors associated with these coefficients provide a measure of the precision of the estimates. The low p-values indicate that all the coefficients are statistically significant, suggesting that they have a significant impact on house prices.

The analysis reveals that a higher grade, less bathrooms, and larger square footage of living space and interior living space among of the nearest 15 neighbors are associated with higher house prices. 



## 3.Conclusions


+ The multiple regression model demonstrates that approximately 53.4% of the variation in house prices can be explained by the included variables: the number of bathrooms, grade, square footage of living space, and square footage of interior housing living space for the nearest 15 neighbors.

+ The highly significant F-statistic of 6000 indicates that the overall model is statistically significant, signifying that the combined effects of the independent variables significantly contribute to predicting house prices.

+ The coefficients offer valuable insights into the relationship between the independent variables and house prices:

     + Each additional bathroom is associated with a decrease of $22,800 in house price, holding other factors constant

     + A higher grade is linked to a higher house price, with each unit increase in grade leading to an increase of $187,900 in price.

     + An increase in the square footage of living space is associated with a higher house price, with each unit increase resulting in an increase of $362,100 in price.

+ More square footage of interior housing living space among the nearest 15 neighbors (sqft_living15) is connected to a higher house price, with each unit increase leading to an increase of $183,000 in price.

+ The normality assumption of the model is satisfied based on the QQ-plot of the model residuals. Additionally, the scatter plot of residuals vs predicted values indicates that the residuals are centered around zero and exhibit random patterns, suggesting that the multiple linear regression assumptions are reasonably met.

+ The low MSE and RMSE values demonstrate the success of this model in predicting house prices in the King County housing market. These results provide confidence in the model's ability to estimate house prices accurately, which can be valuable for buyers, sellers, and real estate professionals in making informed decisions in the real estate market.The difference between the two MSE/RMSE values is relatively small, indicating that the model's performance is consistent across both the training and testing sets.


## 4.Recommenations

_Consumers/Investors_

+ When evaluating house prices, consider the factors included in the multiple regression model: number of bathrooms, grade, square footage of living space, and square footage of the land lots of the nearest 15 neighbors (sqft_living15).

+ Pay attention to the quality and grade of a house, as higher grades are associated with higher prices. This information can be useful when comparing properties or making investment decisions.

+ Consider the impact of square footage of living space on house prices. A larger living space is associated with higher prices, so this factor should be taken into account when assessing property values.

+ While the model indicates that more bathrooms are associated with lower prices, it is important to consider other factors and individual preferences. Some buyers may value additional bathrooms, so it's essential to evaluate the overall appeal and functionality of a property.

_Data Professionals_

+ The model assumes linearity and other assumptions of multiple regression. When making predictions or drawing conclusions, it is crucial to consider these assumptions and their potential limitations.

+ Regularly assess and validate the model's performance using metrics such as MSE. This will help gauge the accuracy and predictive power of the model and identify any potential areas for improvement.

+ There is still room for improvement. It is important to consider additional evaluation metrics and potentially explore other modeling approaches to further optimize the model's performance.

+ Other factors beyond those included in the model may also influence house prices. Consider incorporating additional variables or exploring alternative models to capture a more comprehensive understanding of house price dynamics in the real estate domain.




