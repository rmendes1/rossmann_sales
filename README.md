

<h1 align="center">
    <img alt="RossmannProj" title="#RossmannSales" src="/fig/rossmann_img.png" />
</h1>

<h4 align="center"> 
	🚧 Rossmann Proj 1.0 🚧
</h4>


<p align="center">
  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/rmendes1/rossmann_sales?color=%2304D361">

 <img alt="Repository size" src="https://img.shields.io/github/repo-size/rmendes1/rossmann_sales">
	
  
  <a href="https://github.com/rmendes1/house-rocket/commits/main">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/rmendes1/rossmann_sales">
  </a>

  <img alt="License" src="https://img.shields.io/badge/license-MIT-brightgreen">
</p>



# Table of Contents
<p align="left">
 • <a href="#description">Description</a> </br>
 • <a href="#dataset">Dataset</a> </br>
 • <a href="#tools">Tools</a> </br>
 • <a href="#steps">Steps</a> </br>  
 • <a href="#exploratory-data-analysis-results">Exploratory Data Analysis Results</a> </br>
 • <a href="#machine-learning-models">Machine Learning Models</a> </br>
 • <a href="#error-translation-into-a-business-approach">Error Translation into a Business Approach</a> </br>
 • <a href="#telegram-bot">Telegram Bot</a> </br>	
 • <a href="#conclusion-and-next-steps">Conclusion and Next Steps</a> </br>
 • <a href="#license">License</a>
</p>


# **Description**
_This is a fictional business case_

Rossmann's CFO has done a meeting with all store managers and asked that each of them brought a daily sales forecast of the next 6 weeks.
The CFO needs to make an investiment for stores rebuilding but he does not know how much money he should invest. Therefore, he required
a forecast to know how much the stores will sell and have an idea of the quantity to be invested.

Given the business situation, an important question must be answered:

1. How much revenue will the stores make in the next 6 weeks?

# **Dataset**

- The dataset for this project has been extracted from Kaggle's Rossmann Prediction Sales' competition. 
- This dataset an all the pieces of information regarding it can be found at https://www.kaggle.com/c/rossmann-store-sales

## Files and Attributes

| Files     | Description                                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| train.csv             | historical data including Sales |
| test.csv             | historical data excluding Sales |
| sample_submission.csv             | a sample submission file in the correct format |
| store.csv             | supplemental information about the stores |

- Most of the data fields are self-explanatory. The following are descriptions for those that aren't.


| Attributes     | Meaning                                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id             | an Id that represents a (Store, Date) duple within the test set                                                                                                                                                                         |
| Store           | a unique Id for each store                                                                                                                                                                                |
| Sales          | the turnover for any given day (this is what you are predicting)                                                                                                                                                                              |
| Customers       | the number of customers on a given day                                                                                                                                                                                  |
| Open     | an indicator for whether the store was open: 0 = closed, 1 = open            |
| StateHoliday    | indicates a state holiday. Normally all stores, with few exceptions, are 		closed on state holidays. Note that all schools are closed on public holidays and weekends. a = public holiday, b = Easter holiday, c = Christmas, 0 = None                                                                                                                                               |
| SchoolHoliday             | indicates if the (Store, Date) was affected by the closure of public 	schools
|	StoreType | differentiates between 4 different store models: a, b, c, d |                                                                                                                                                                     |
| Assortment        |describes an assortment level: a = basic, b = extra, c = extended                                                                                                                                                                                    |
| CompetitionDistance     |  distance in meters to the nearest competitor store                                                                                                         |
| CompetitionOpenSince[Month/Year]           | gives the approximate year and month of the time the nearest competitor was opened                                                                                                                                        |
| Promo      | indicates whether a store is running a promo on that day                                                                                                                                              |
| Promo2          | Promo2 is a continuing and consecutive promotion for some stores: 0 = store is not participating, 1 = store is participating |
|Promo2Since[Year/Week]     | describes the year and calendar week when the store started 	participating in Promo2  |                                                                                                                        
| PromoInterval  | describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. "Feb,May,Aug,Nov" means each round starts in February, May, August, November of any given year for that store  |                                                                                                                        

# **Tools**
![Python](https://img.shields.io/badge/-Python-007396?style=flat-square&logo=python&logoColor=ffffff)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-FFA500?style=flat-square&logo=jupyter&logoColor=ffffff)
![Heroku Cloud](https://img.shields.io/badge/-Heroku%20Cloud-7F00FF?style=flat-square&logo=heroku&logoColor=%23ffffff)

# **Steps**
In this project we will follow the CRISP-DM Proccess of Development, which consists in:
- **Business understanding**
  - _What is the motivation?_
  - _What is the problem cause?_
  - _What is the solution format?_
- **Data collection (via Kaggle)**
- **Data Cleaning**
  - Descriptive Statistics Analysis: Mean, Median, Max, Min, Standard Deviation, Inter-Quartile Range, Skewness, Kurtosis.  
  - Feature Engineering: To obtain new values that are required for better inferences based on the previous values obtained.
  - Data Filtering/Selection: To select the rows, columns, and data ranges that are not relevant for the model or are outside the business scope.
- **Data Exploration**
  - _What variables affect this fenomena?_
    - Univariate Analysis
    - Bivariate Analysis
    - Multivariate Analysis
- **Data Preparation/Modelling**
  - Rescaling: To normalize all data (numerical and categorical) to the same scale for the ML Model to be trained. 
  - Variable Filtering/Selection: To select the variables that are more relevant for the prediction model. **Boruta Feature Selector** was used here to define the best variables.
- **ML Algorithms implementation**
  - Set the models to be used and calculate their performances for this specific problem. 
- **Hyperparameter Fine-tuning**
  - To find the conjunct of parameters that maximize the model learning process.
- **Interpretation of the ML Algorithm and Error translation**
  - To estimate if the model is accurate enough and tell how much revenue it will bring to the company.  
- **Project Deploy on /Heroku Cloud**
  - To publish the model in a cloud environment so others can have access to it.   
- **Creation of a Telegram Bot**
  - To enable the stores revenue query at any time using your Telegram account. 


# **Exploratory Data Analysis Results**
- For the purpose of briefness, only the univariate and multivariate analysis are showed in this readme. For more info, check https://github.com/rmendes1/rossmann_sales/blob/main/eda.ipynb.

## Univariate Analysis
<p align = "center">Image 1 - Response Variable Distribution</p>
<img alt="RossmannProj" title="#ResponseVariable" src="/fig/response_variable_UA.png" />
<p align = "center">Image 2 - Numerical Variables Distribution</p>	
<img alt="RossmannProj" title="#NumericvalVariables" src="/fig/num_variables_UA.png" />
<p align = "center">Image 3 - Categorical Variables Distribution</p>
<img alt="RossmannProj" title="#CategoricalVariables" src="/fig/cat_variables_UA.png" />


## Multivariate Analysis
<p align = "center">Image 4 - Pearson Correlation for Numerical Variables</p>
<img alt="RossmannProj" title="#ResponseVariable" src="/fig/corr_MA_numerical.png" />
<p align = "center">Image 4 - Cramer's V matrix for Categorical Variables</p>
<img alt="RossmannProj" title="#ResponseVariable" src="/fig/corr_MA_categorical.png" />


# **Machine Learning Models**
## Performance Results
For this project, 5 models were trained and had their performances compared:
 - Average Model
 - Linear Regression Model
 - Linear Regression Regularized Model (Lasso)
 - Random Forest Regressor
 - XGBoost Regressor

The results after cross-validation has been performed were:
<p align = "center">Image 5 - ML Algorithms Performance Comparison </p>
<img alt="RossmannProj" title="#Machine Learning Algorithms Results" src="/fig/ML_results_1.png" />

Even though the Random Forest Regressor had the best model performance reached, we will select
XGBoost for the analysis, since it is less robust in terms of memory space in our local machine and the differences in performance are not so distant. However, in a server application scenario, Random Forest Regressor would be the most preferable choice.

## Hyperparameter Fine-tuning
Random search was used to find optimal parameters, which gives us the following result:
<p align = "center">Image 6 - ML Algorithms Performance Comparison </p>
<img alt="RossmannProj" title="#Hyperparameter Fine-tuning" src="/fig/model_tuning.png" />

# **Error Translation into a Business Approach**
After all these steps, it is time to answer the question we were here for: _How much revenue will the stores make in the next 6 weeks?_
This table was generated to show some store samples of the model prediction comparing them with their most optimistic/pessimistic revenue and their respective error rate.

<p align = "center">Image 7 - ML Algorithms Performance Comparison </p>
<img src="/fig/prediction_samples.png" />

As a more general analysis, down below is the total revenue that would be done by the stores and the prediction plot.

<p align = "center"> Image 8 - Final Revenue Scenario </p>
<p align = "center"> <img src="/fig/total_scenario.png" />  </p>

<p align = "center">Image 9 - Predictions over time </p>
<img src="/fig/prediction_plot.png" />

# **Telegram Bot**
To access the bot contact, click here:

[![Telegram](https://img.shields.io/badge/-TELEGRAM-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/rossmannjr_bot)


To use the bot, you need to type the store number in the chat. Then, the bot will tell you the prediction for that store.
If the store number does not exist, it will show the store is not available for query.

<p align = "center">Image 9 - Predictions over time </p>
<img alt="RossmannProj" title="#TelegramBot" src="/fig/bot_print.png" />

# **Conclusion and Next Steps**
- Given that this is the first CRISP-DM iteration cycle, there is a relatively good performance, considering the error to be approximately 10% (MAPE).
- Some stores have higher error values that can be improved in the next cycle separetely.
	

# **License**

This project is under MIT License.

Done with ❤️ by João Renato Mendes 👋🏽 [Get in touch!](https://www.linkedin.com/in/joaorenatomendes/)

_This readme is in progress_
