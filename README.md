# Predicting Rock Climbing Performance

## Description
The primary goal of this project was to predict how well a person would be climbing one month from now given what they've climbed in the past, how often they climbed, and demographic information. In addition to making that model, I also explored the question, "What does it mean when someone says that they climb a particular grade, and does that differ by gender?"

## Data Used
Information was scraped from 3,960 users off of [Mountain Project's Partner Finder](https://www.mountainproject.com/partner-finder) page. The resulting data frame had 514,921 rows, where each row represented a tick by a user.

## Features and Target
Features scraped: 
* From the partner finder page: age, gender, location, membership date, lead grades and follow grades for every type of climb a user listed, other interests of the user, times the user is available to climb.
* From the user's page: membership
* From the user's CSV file: date of each tick, route name, type of climb, grade of each route, stars given by the user, average stars for the route, grade of the route, grade given by the user.

Features ultimately used in model: Max grade of this month, max grade of last month, and max grade of two months ago.

Target: The max grade of next month.

## Tools and Modeling
Tools used: Selenium, Pandas and Numpy, Seaborn, Matplotlib, Sklearn, Voila, Tensorflow

Modeling: Linear Regression, Random Forest Regression, Neural Network.
Best Model: Random Forest Regression.
Final scores: RMSE - 2.4. R-squared - .52

## Voila

