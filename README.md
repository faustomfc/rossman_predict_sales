# ROSSMANN PREDICT SALES
This project aims to predict the sales of the Rossmann stores for the next 6 weeks.

**Project link:** https://www.kaggle.com/competitions/rossmann-store-sales/

## 1) Understanding the business and its problem
Rossmann operates over 3,000 drug stores in 7 European countries. Currently, Rossmann store managers are tasked with predicting their daily sales for up to six weeks in advance. Store sales are influenced by many factors, including promotions, competition, school and state holidays, seasonality, and locality. With thousands of individual managers predicting sales based on their unique circumstances, the accuracy of results can be quite varied. So it's necessary to develop a Data Science Project that predict the Rossmann sales with a good accuracy.

## 2) Data description
The following description for each feature:

**Id** - an Id that represents a (Store, Date) duple within the test set;

**Store** - a unique Id for each store;

**Sales** - the turnover for any given day (this is what you are predicting);

**Customers** - the number of customers on a given day;

**Open** - an indicator for whether the store was open: 0 = closed, 1 = open;

**StateHoliday** - indicates a state holiday. Normally all stores, with few exceptions, are closed on state holidays. Note that all schools are closed on public holidays and weekends. a = public holiday, b = Easter holiday, c = Christmas, 0 = None;

**SchoolHoliday** - indicates if the (Store, Date) was affected by the closure of public schools; Planejamento do projetoOs

**StoreType&** - differentiates between 4 different store models: a, b, c, d

**Assortment** - describes an assortment level: a = basic, b = extra, c = extended

**CompetitionDistance** - distance in meters to the nearest competitor store

**CompetitionOpenSince** - gives the approximate year and month of the time the nearest competitor was opened

**Promo** - indicates whether a store is running a promo on that day

**Promo2** - It's a continuing and consecutive promotion for some stores: 0 = store is not participating, 1 = store is participating

**Promo2Since** - describes the year and calendar week when the store started participating in Promo2

**PromoInterval** - describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. "Feb,May,Aug,Nov" means each round starts in February, May, August, November of any given year for that store

## 3) Project planning
The project was developed based on the CRISP cycle methodology. It's divided in 10 parts: Data description, Feature engineering, Data filtering, Exploratory data analysis (EDA), Data preparation, Feature selection, Machine learning modelling, Hyperparameter fine tuning, Error interpretation and Deploy model to production.

The Machine Learning models used were Average, Linear Regression, Linear Regression Regularazied (LASSO), Random Forest Regressor and XGB Regressor. The error parameters used was Mean Absolute Error (MAE), Mean Absolute Percentage Error (MAPE) and Root Mean Square Error (RMSE).

## 4) Results description
The EDA provided the observation that the featues didn't have the behaviour of a normal distribution. So in the data preparation some techniques of transformation of the data was necessary to adequate the features in normal distribution. The bivariate analysis provided some hypothesis tests that gave important business insights like "stores with larger assortment sell less".

The machine learning modelling section showed that XGBoost Regressor could predict better the purposed objective for this project. After hyperparameter fine tuning, XGBoost Regressor got a real performance (cross validation) of MAE 625.97, MAPE 0.0923 and RMSE 920.14, with a Mean Percentage Error of -0.00902.
