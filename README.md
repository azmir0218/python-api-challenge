# Python API - What's the Weather Like?

## Part I - WeatherPy

In this example, we will be creating a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, we will be utilizing a [simple Python library](https://pypi.python.org/pypi/citipy), the [OpenWeatherMap API](https://openweathermap.org/api), and a little common sense to create a representative model of weather across world cities.

First we will create a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude

After each plot, we will add a sentence or two explaining what the code is analyzing.

Second we will run linear regression on each relationship. This time, we will separate the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

After each pair of plots, we will take the time to explain what the linear regression is modeling. For example, describing any relationships we notice and any other analysis we may have.

Finally we will:

* Randomly select **at least** 500 unique (non-repeat) cities based on latitude and longitude.
* Perform a weather check on each of the cities using a series of successive API calls.
* Include a print log of each city as it's being processed with the city number and city name.
* Save a CSV of all retrieved data and a PNG image for each scatter plot.

### Part II - VacationPy

* Created a heat map that displays the humidity for every city from Part I.

  ![heatmap](https://github.com/azmir0218/python-api-challenge/blob/main/WeatherPy/Screen%20Shot%202021-10-23%20at%209.04.18%20PM.png)

* Narrowed down the DataFrame to find ideal weather condition. For example:

  * A max temperature lower than 80 degrees but higher than 70.

  * Wind speed less than 10 mph.

  * Zero cloudiness.

  * Dropped any rows that don't contain all three conditions. We want to be sure the weather is ideal.

* Used Google Places API to find the first hotel for each city located within 5000 meters of our coordinates.

* Ploted the hotels on top of the humidity heatmap with each pin containing the **Hotel Name**, **City**, and **Country**.

  ![hotel map](Images/hotel_map.png)

## Tools Used:

Jupyter Notebook, Python, Numpy, Scipy, API's, Gmaps
