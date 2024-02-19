# Statistical Analysis of Grocery Data

## Table of contents

- [Overview](#overview)
- [Libraries](#libraries)
- [Process](#process)
  - [Data Analysis](#data-analysis)
  - [Linear Regression](#linear-regression)
  - [K-Means Clustering](#k-means-clustering)
- [Summary](#summary)
- [Acknowledgments](#acknowledgments)

## Overview
This project is part of my academic studies for the subject Data Mining for Business Intelligence.
Within the scope of this project, each participant was arbitrarily allocated a database characterized by multiple tables. The primary objective was to apply both a supervised and an unsupervised data mining technique to conduct a comprehensive analysis of the database.

We decided to use Linear Regression as the supervised technique and K-Means Clustering as the unsupervised technique.

## Libraries
- pyodbc: Used to enable access to ODBC (Open Database Connectivity) databases
- pandas: Used for data manipulation and data analysis
- matplotlib: Used to create basic graphs
- seaborn: Statistical data visualization library based on matplotlib
- sklearn: Used for splitting data into train-test sections and for statistical analysis like LinearRegression, KMeans

## Process

There were about 20 different tables in this database. After going through all of them, the best table was the Product Table because it had more features that could help us predict something. This could be quickly done by plotting a scatter plot matrix and seeing if there are any visible clusters or patterns

![image](https://github.com/MayuraRane/Grocery-Analysis-Python/assets/42894788/8547d84b-7837-45a8-a2c0-e6aa097f7507)

### Data Analysis

First, we checked for null values and deleted those records.
Next, we created a correlation matrix to check which features are more related:
![image](https://github.com/MayuraRane/Grocery-Analysis-Python/assets/42894788/7b1578de-4685-496d-a519-80179fc5e2a0)

We can see here that Total_Fat_G and Carbohydrates_G are highly correlated to Calories

### Linear Regression
<br>
<img src="https://github.com/MayuraRane/Grocery-Analysis-Python/assets/42894788/2e923c49-c068-4f0b-a6e9-210edd5c2b81" height="300"><br>
<br>
<img src="https://github.com/MayuraRane/Grocery-Analysis-Python/assets/42894788/c9fbd823-d2f5-45f2-a6a3-96ca9aef6f3a" height="300"><br>

### K-Means Clustering

We checked the correlation matrix and couldn't see any prominent clusters but we considered this:
<br><img src="https://github.com/MayuraRane/Grocery-Analysis-Python/assets/42894788/e68a3e31-05b4-431d-8515-53e087a89cf2" height="400"><br>

After applying clustering techniques, we were getting weird outputs. Thus we decided to use the elbow method to calculate the optimal number of clusters:
<br><img src="https://github.com/MayuraRane/Grocery-Analysis-Python/assets/42894788/fcd8230a-3b9c-480c-8862-47d33921d4a6" height="300"><br>

According to the above graph, we decided to show 2 clusters. There are no clusters in this dataset but we forced them for the sake of the project's goal:
<br><img src="https://github.com/MayuraRane/Grocery-Analysis-Python/assets/42894788/463a76b1-0059-49d7-ab8c-b3dd746548eb" height="300"><br>


## Summary

Overall, we learned about correlation matrix, scatter plots, linear regression, and k-means clustering.


## Acknowledgments

This was part of my Master's project on the subject of Data Mining for Business Intelligence taught by Bill Nicholson. 
It was a group project with Monica Varu and Wenhan Zu.
