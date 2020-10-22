# API-Challenge

**WeatherPy**

This challenge involves using a new library citipy that provides geocoordinates for available cities
with population over 500

## General info
Utilized the open weather api to get weather data for random cities list generated using citipy library.

## Technologies
* jupyter notebook - version 6.0.3

## Code Examples

Data Cleaning:

1.created a cities list to hold a random city & tested it against query url for exception handling to identify a fake city.
2.appended(0) to the list for values returned by fake cities.
3.cleaned the dataframe by retaining the rows that have non-zero values.
4.saved the file as csv.

``cities=["New York", "London","Boslo Fake City","Moscow","Beijing"]
``for city in cities:
    url= query_url + city
    time.sleep(1)
    try:
        response=requests.get(url).json()
        lat.append(response["coord"]["lat"])
	except KeyError:
        #print("City not found")
        lat.append(0)
        lng.append(0)
``cleaned_df=df.loc[df["Lat"]!=0]``


 Data Plotting:
 
 1.plotted scatter plots using the dataframe created from the csv file.
 ``x=pd.to_numeric(df['Lat'])
 ``y=pd.to_numeric(df['Max Temp (F)'])
 2.saved the figures as .png files.
 ``plt.savefig(r"output_files\LatvMaxTemp.png")``
 
 Linear Regression:
 
1.created two new dataframes for northern and southern hemisphere lat values.
2.plotted the linear regression lines & entered correlations based on the findings.


**VacationPy**

This challenge involves using jupyter-gmaps & google places API to generate humidity heat maps & ideal vacation cities with marker layer.

## General info
Utilized the .csv file generated in WeatherPy assignment.

## Technologies
* jupyter notebook - version 6.0.3

## Code Examples

Data Cleaning:
1.from main dataframe, created a new dataframe that has columns for Lat & Lon.

 Humidity Heat Map:
 1.used gmaps to generate the base map.
 2.passed the Lat and Lon columns as inputs to locations & humidity as weights.
 3.added a heat map layer & saved the figure as .png file.
 
 Weather Fitting Criteria:
 1.created new dataframe matching the ideal weather criteria.
 2.used google places api to search for nearby hotels.
 3.added markup layer to the humidity heat map showing the hotel markups.
 4.saved the figure as .png file.
 