# API-Challenge

## **WeatherPy**

	This challenge introduced a new library citipy that provides geocoordinates for available cities with population over 500.
## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Code Examples](#codeexamples)


## General info
	Utilized open weather api to get weather data for random cities list generated using citipy library.

## Technologies
* jupyter notebook - version 6.0.3

## Code Examples

	Data Cleaning:

	1.defined a random list of actual cities & a fake city & ran it against query url to test exception handling for fake city.  
	2.exception handled by appending 0 or 'city not found'.  
	3.cleaned the dataframe by retaining the rows that have non-zero values.  
	4.saved the file as csv.  

``cities=["New York", "London","Boslo Fake City","Moscow","Beijing"]``
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
 
	1.plotted scatter plots using pandas & csv file as input.  
 ``x=pd.to_numeric(df['Lat'])``
 ``y=pd.to_numeric(df['Max Temp (F)'])``
	2.saved the figures as .png files.
 ``plt.savefig(r"output_files\LatvMaxTemp.png")``
 
 Linear Regression:
 
	1.created two separate dataframes, one for cities in northern hemisphere & one for cities in southern hemisphere.  
	2.plotted linear regression lines & entered correlations based on findings.  


##** VacationPy**

	Used jupyter-gmaps & google places API to generate humidity heat maps with marker layer.  
## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Code Examples](#codeexamples)


## General info
	Utilized .csv file generated in WeatherPy assignment.  

## Technologies
* jupyter notebook - version 6.0.3

## Code Examples

 Humidity Heat Map:
	1.used gmaps to generate the base map.  
	2.passed Lat and Lon column values as inputs to locations & humidity column values as weights.  
	3.added a heat map layer & saved the figure as .png file.  
 
 Weather Fitting Criteria:
	1.created new dataframe matching the ideal weather criteria.  
	2.used google places api to search for nearby hotels.  
	3.added markup layer to the humidity heat map showing the hotel markups.  
	4.saved the figure as .png file.  
 