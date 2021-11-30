# Real-Estate
Real estate prediction

# 1. Business Problem
## 1.1 Problem Context

I am a beginner data scientist and also a person who wants to buy a house. With this project I want to try to predict the price of the apartments in capital of Kyrgyzstan - Bishkek.

## 1.2 Problem Statement
* The data was collected in 2021.
* The task is to build a real-estate pricing model using that dataset.
* I want to build a model to predict transaction prices with an average error of under US Dollars 5 000.

## 1.3 Business Objectives and Constraints
* Deliverable: Trained model file
* Win condition: Avg. prediction error < \$5,000

# 2. Machine Learning Problem
## 2.1 Data Overview

For this project:

* The dataset has 1883 observations in Bishkek.
* Each observation is for the transaction of one property only.
* Each transaction was between $30,000 and $120,000

### Target Variable
'tx_price' - Transaction price in USD

### Features of the data:

Property characteristics:

Property characteristics:
* 'beds' - Number of bedrooms
* 'baths' - Number of bathrooms
* 'sqft' - Total floor area in squared feet
* 'year_built' - Year property was built

Location convenience scores:
* 'restaurants' - Number of restaurants within 1 mile
* 'groceries' - Number of grocery stores within 1 mile
* 'cafes' - Number of cafes within 1 mile
* 'shopping' - Number of stores within 1 mile
* 'beauty_spas' - Number of beauty and spa locations within 1 mile
* 'active_life' - Number of gyms, yoga studios, and sports venues within 1 mile

Schools:
* 'num_schools' - Number of public schools within district
* 'median_school' - Median score of the public schools within district, on the range 1 - 10

## 2.2 Mapping business problem to ML problem
### 2.2.1 Type of Machine Learning Problem
It is a regression problem, where given the above set of features, we need to predict the transaction price of the apartment.

### 2.2.2 Performance Metric (KPI)
**Since it is a regression problem, we will use the following regression metrics:**
* Root Mean Squared Error (RMSE)
* R-squared
* Mean Absolute Error

# 3.Feature Engineering

### 3.1.Features Created:

##### old_properties:
* People might also not take much interest in old properties.
* so, this feature gives properties built before 1980.

##### school_score:
* A school score feature is created as num_schools * median_school

##### One hot Encoding:
* Machine learning algorithms cannot directly handle categorical features. Specifically, they cannot handle text values.
* Therefore, we need to create dummy variables for our categorical features.
* *Dummy variables* are a set of binary (0 or 1) features that each represent a single class from a categorical feature.















