

<h1 align="center">
    <img alt="RossmannProj" title="#RossmannSales" src="rossmann_img.png" />
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
<p align="center">
  <a href="#description">Description</a> •
  <a href="#dataset">Dataset</a> •
  <a href="#tools">Tools</a> •
  <a href="#steps">Steps</a> •  
  <a href="#conclusion">Conclusion</a> •
  <a href="#next-steps">Next Steps</a> •
  <a href="#license">License</a>
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

- Files

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

# Tools
![Python](https://img.shields.io/badge/-Python-007396?style=flat-square&logo=python&logoColor=ffffff)
![SQLite](https://img.shields.io/badge/-SQLite-5CB3FF?style=flat-square&logo=sqlite)

# Steps
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
- **Hyperparameter Finetuning**
  - To find the conjunct of parameters that maximize the model learning process.
- **Interpretation of the ML Algorithm and Error translation**
  - To estimate if the model is accurate enough and tell how much revenue it will bring to the company.  
- **Project Deploy on /Heroku Cloud**
  - To publish the model in a cloud environment so others can have access to it.   
- **Creation of a Telegram Bot**
  - To enable the stores revenue query at any time using your Telegram account. 

# Conclusion
- TBD
	
	
# Next steps
- TBD

# License

This project is under MIT License.

Done with ❤️ by João Renato Mendes 👋🏽 [Get in touch!](https://www.linkedin.com/in/joaorenatomendes/)

_This readme is in progress_
