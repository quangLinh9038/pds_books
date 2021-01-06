# Practical Data Science
# Assignment 2: Data Modelling
# Due date: Jan 4, 2020


# Data Modelling Instructions: 

# Goals: Predict average rating of books which are scarped from "Best Book Ever" dataset


# Task 1: Data Preparation: 

I firstly encoding datatset with 'UTF-8' when reading dataset for all X_train, X_test and 'ASCII' encoding for y_train. This decrease unreadable values and make it easier to read and define. 

Next, I will hanlde missing values for each datasets with imputing fillna() functions ('none' for object datas and '0' for numerical data). 

Due to specific goal of predicting rating, several columns are dropped in very first place to handle datasets more efficiently. 

Eachh columns are cleand with cleaning regular expression, stripin out whitespaces and lowercasing. Because non-numerical features has many unique multivalues, I handled with formating them into single values that could affect on the final result. 

# Task 1.2: Data Exploration 

I visualiza numerical data by histogram to view their data distributed whether being skewness. 

Afterwards, some scatterplots are displayed to show the relationship between the target feature (avg_rating) to categorical features. 
 
I observed that 'rating_count' and 'review_count' are not normally distributed then fixing skewness and append them into X_train as well as drop original columns. 

# Task 2: Feature Engineering

Using Label Encoder to encode categorical features

Applying TF-IDF to mining textual in 'description' feature.

# Task 3: Data Modelling

Using TF-IDF, XgBoost with Sentiment scores and Linear Regression models to train and predict featured datasets.