# Module 2 Linear Regression

Introduction:

For this project, I worked with a (canada_rent.csv) containing rental prices for diverse units across Canada in 2024.

My goal is to explore multiple regression models, in order to find a model that predicts the rental price most accurately. 
In this project, I will be comparing a Linear Regression Model, a Simple Polynomial Model, and an ElasticNetCV Model.

## Project Outline

1. The project will begin with an EDA portion to better understand the data, indentify trends, and determine important features useful for regression models.
2. Data will be cleaned and prepared for visualization.
3. Once data has been organized and cleaned, visualization will be included to support my analysis of aforementioned trends. Key variables will be determined for feature engineering.
4. Proceed with feature engineering to formulate three(3) regression models.
5. Compare different regression models & distinguish which will best predict prices.
6. Use final model to make new predictions.

### The criteria for project submission were the following:

- You will upload your completed project in a PUBLIC Github repository in your account.
- Your repository MUST include:
  - a README.md page that includes a description and summary of your analysis.
  - The completed .ipynb notebook with your analysis.
- Your notebook has to be organized and clean. Break down your steps, and follow coding best practices.

*Exploratory Data Analysis (EDA)*

Performed EDA to understand dataset distribution, trends, and relationships. Used a few visualizations to detect key trends.

Identified missing values, outliers, and categorical/numerical feature distributions. In different cases, adjusted missing values by filling with mode, mean or dropping unnecessary values.

*Feature Engineering*
 
Encoded selected columns to numerical values from object, and selected features among them to use for regression modelling.

*Regresion Modelling*

The target variable for all modelling is the price since that is the prediction intended. Using a test size of 15%, 85% for training.

**1st Model: Linear Regression**

- The first model is scaled using StandardScaler. The validation values are all quite high, specifically MSE.

**2nd Model: Polynomial Regression**

- The second model is scaled as well using StandardSCaler. The validation values are more reliable than the previous linear regression model. R2 score is improved from the first; confidence rises with this model predicting prices.

**3rd Model: ElasticNetCV Polynomial Regression**

- The third and final model I chose to use was ElasticNetCV due to its ability to stabilize large datasets, such as this rental market. Ultimately, this model did not outperform the Polynomial Regression, but it came close.

## Conlcusion and Final Model Prediction

*Final Model*

I chose to predict outcomes of select features for price with the polynomila regression model. The table I created in the final portions of the notebook reflect that this model best fit the dataset. It is not overfitting the data, but the values are all quite low.
The input selection I chose is to predict price according to a unit with 2 baths (coefficient 572.104667) and 1200 square feet (coefficient 0.859046). The model predicted that a unit of this make would be equivalent to 3453$ +- 711$ depending on location in Canada.
