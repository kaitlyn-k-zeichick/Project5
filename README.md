# Predicting Rock Climbing Performance

## Description
The primary goal of this project was to predict how well a person would be climbing one month from now given what they've climbed in the past, how often they climbed, and demographic information. In addition to making that model, I also explored the question, "What does it mean when someone says that they climb a particular grade, and does that differ by gender?"

## Applications
I envision the prediction model as a part of a much bigger project. For the bigger project, I'm envisioning an indoor climbing gym. At the top of each route of the climbing gym is a device, such as a raspberry pi, that stores the grade of the route. The climbers at the gym would all have bracelets, and when they reached the top of the climb they would tap the bracelet to the raspberry pi. The pi would then store that information in an app, so that the climber could keep track of what climb they’ve done and on what day.
This project builds out the predictive part of the app. Oftentimes climbers will hit plateaus in how hard they can climb, and seeing a graph that shows potential improvement would be a motivator for climbing more. 

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
After I'd trained a model, I created an web app through Voila where users can input what grades they've climbed in the past and see what the model predicts that they'll be climbing next month. It also shows a graph of what they've climbed in the past and the model prediction. This is what it currently looks like:

<img width="574" alt="Screen Shot 2021-03-25 at 2 40 47 PM" src="https://user-images.githubusercontent.com/74684202/112547546-1d2ccf80-8d78-11eb-93ed-1865f5f90c00.png">

To run the app, first [install Voila](https://github.com/voila-dashboards/voila). Then download the 'Using Voila' notebook. From the terminal, move to the same directory as the notebook, and then type 'voila 'Using Voila.ipynb.'

## What does it mean when someone says that they climb a particular grade?

In climbing, people will often say, "I climb 5.10a" or "I lead 5.11b," but there's no actual rules for what this means. It could mean that they've climbed that grade once in their entire life, or it could mean they've done hundreds of routes at that grade. To explore this topic, I conducted some analyses in the 'Defining what people climb.ipynb' notebook. I also wrote a blog analyzing the results titled [Defining What You Climb: 'Am I a 5.11a climber yet?](https://kaitlynzeichick.medium.com/defining-what-you-climb-am-i-a-5-11-climber-yet-675c0f9fe2f8). 

The results showed that on average, when a climber says that they climb a certain grade, that means that they've climbed it 6.3 times. But there's a disparity between men and women. The average man who claims to lead a certain grade has climbed that grade 5.9 times. The average woman who claims to lead a certain grade has climbed that grade 7.7 times.

The results also showed that people tend to say that they climb grades that end in 'a', like 5.10a or 5.11a, more often than grades that end in 'b', 'c', or 'd'.

