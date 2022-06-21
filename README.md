# Regression-Portfolio

<br>
TO DO:
- Update ReadMe File for Predictive Models and Model Evaluation
<br>

## General Overview
This Portfolio project is comprises the analysis of fare-prices of Uber rides in New York City, USA. The dataset was obtained from Kaggle: https://www.kaggle.com/datasets/yasserh/uber-fares-dataset

This project was carried out strictly for educational purposes;

The chosen dataset comprises data about Uber Rights, mainly in New York City (NYC) 
The dataset comprises 8 columns:
- key - a unique identifier for each trip
- fare_amount - the cost of each trip in $
- pickup_datetime - date and time when the meter was engaged
- passenger_count - the number of passengers in the vehicle (driver entered value)
- pickup_longitude - the longitude where the meter was engaged
- pickup_latitude - the latitude where the meter was engaged
- dropoff_longitude - the longitude where the meter was disengaged
- dropoff_latitude - the latitude where the meter was disengaged

<br>

## Aim and Objective

The dataset contains a variety of information, including pick-up/drop-off locations, passenger count and price for Uber rides in NYC. <br>The goal of this analysis is to <strong>develop an array of regression models which can be used to predict the price of an Uber ride, based on location, distance, passenger count and date.</strong>


<br>

## Exploratory Data Analysis

Several steps to get an initial overview of the data have been taken, including:<br>
- Dropping unnecessary columns (e.g. the “key” columns)
- Determining the object type of each column (using a custom developed function)
- Determining the number of unique values of each column (using a custom developed function)
- Determining the number of null values of each column (using a custom developed function)
- Splitting the datetime column into individual year, month, day, day_of_week, hour, minute & second columns

<br>

- A custom function was written to calculate the distance between pick-up point and drop off point based on the coordinates
- Using the Folium library, pick-up and drop-off point were visualized on a map, as shown below. The individual points were clustered geographically to ensure the visualization is more simple and visually appealing.

<br>

<img width="1595" alt="image" src="https://user-images.githubusercontent.com/77542239/174909956-97672b71-f7a7-4a96-b804-1114130d4c6b.png">

<br>

As can be seen, the vast majority of data points is located in NYC; however, some pick-up points are located in other places, including being located in the ocean. Since >99% of data points were correctly located in NYC, it was assumed that the remaining coordinates are simply wrong/falsely captured data points. <br> <br>
=> These data points/observations were then excluded. To exclude those observations, a function was written to filter out observations that are outwith of NYC metropolitan area.
<br> <br>

Finally, it was recognized that some of the variables are objects and need to be encoded. Here, <strong>One-Hot-Encoding</strong> was used, and the following columns were encoded:  year, month, day, hour, day of week.<br>
Reasoning: Days are not ordinal numbers. Just because it is the 20th of a month it does not necessarily represent an effect that is 20x as strong as on the first of a month.

<br>

## Predictive Models
### Linear Regression
### Linear Regression with Polynomial Features
### Linear Regression with Polynomial Features and Regularization

<br>

## Model Evaluation
- A custom function was written to visualize performance of the models

<br>
<img width="1000" alt="image" src="https://user-images.githubusercontent.com/77542239/174911471-8550d8cb-d01a-4225-a72f-4a12f2665122.png">
