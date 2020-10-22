# API-Challenge
API homework

> WeatherPy
This challenge involves using a new library citipy that provides geocoordinates for available cities
with population over 500

## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Code Examples](#codeexamples)

## General info
Utilized the open weather api to get weather data for random cities list generated using citipy library .

## Technologies
* jupyter notebook - version 6.0.3

## Code Examples

`Data Cleaning:
-created a cities list to hold a random city & tested it against query url for exception handling to identify a fake city
-appended(0) to the list for values returned by fake cities. cleaned the dataframe by retaining the rows that have non-zero values
-saved the file as csv

 Data Plotting:
 -plotted scatter plots using the dataframe that was created from the csv file
 -saved the figures as .png files
 
 Linear Regression:
 
 -created two new dataframes for northern and southern hemisphere lat values.
 -plotted the linear regression lines & entered corelations based on the findings.
 
 VacationPy
This challenge involves using jupyter-gmaps & google places API to generate humidty heat maps & 

## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Code Examples](#codeexamples)

## General info
Utilized the open weather api to get weather data for random cities list generated using citipy library.

## Technologies
* jupyter notebook - version 6.0.3

## Code Examples

`Data Cleaning:
-used the final_cities.csv file from WeatherPy/
-cleaned dataframe & retained lat and lng values 

 Humidity Heat Map:
 -used gmaps to generate the map.
 -saved the figure generated as .png file
 
 Weather Fitting Criteria:
 -created new dataframe matching the ideal weather criteria.
 -used google places api to search for nearby hotels.
 -added markup layer to the heat map.
 