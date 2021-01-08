
<p align="center">
 <h2 align="center"> Python API Challenge </h2>
 <h1 align="center"> What's the Weather Like? </h1>
</p>

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#background">Background</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#part-one-weatherpy">Part One - WeatherPy</a>
      <ul>
        <li><a href="#python-notebook">Python Notebook</a></li>
        <li><a href="#scatter-plots">Scatter Plots</a></li>
        <li><a href="#linear-regression-plots">Linear Regression Plots</a></li>
        <li><a href="#dataframe">Dataframe</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>

<!-- Background -->
## Background

Using Python requests, APIs, and JSON traversals, Part I of this project examines weather patterns as we approach the equator. While we know the temperature gets hotter, we will also evaluate humidity, windspeed, cloudiness, in addition to max temperature, to understand how latitude affects weather. Part Two of this project will use jupyter-gmaps and the Google Places API to plan a future vacation based on the data collected in Part One. This python project was completed as a part of Georgia Tech's Data Science and Analytics boot camp.

### Built With
* [Python](https://www.python.org/)
* [CitiPy](https://pypi.python.org/pypi/citipy)
* [OpenWeatherMap API](https://openweathermap.org/api)


## Part One - WeatherPy

In order to visualize the weather of 500+ cities across the world of varying distance from the equator, we will utilize citipy, a [simple Python library](https://pypi.python.org/pypi/citipy) and the [OpenWeatherMap API](https://openweathermap.org/api) to help create a representative model of weather across world cities.

### Python Notebook
To view the python code used to extract and transform the data, select the link below to view the full notebook.
* [Weather Py Jupyter Notebook](https://nbviewer.jupyter.org/github/asmvm/Python_API_Challenge/blob/master/Weather_Py/WeatherPy_main.ipynb)

### Scatter Plots
Scatter plots illustrating relationship between temperature, humidity, cloudiness, and windspeed vs latitude. Max Temp displayed below. Select links to plots to view remaining plots:

![Temperature (F) vs. Latitude](saved_figures/lat_vs_maxtemp.png)
* [Humidity (%) vs. Latitude](saved_figures/lat_vs_humidity.png)
* [Cloudiness (%) vs. Latitude](saved_figures/lat_vs_cloudiness.png)
* [Wind Speed (mph) vs. Latitude](saved_figures/lat_vs_windspeed.png)


### Linear Regression Plots
Linear regression is run on each relationship, while also looking at cities in Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude). A linear regression function was created to optimize the code when creating the plots:

![Northern Hemisphere - Temperature (F) vs. Latitude](saved_figures/northernhem_maxtemp_vs_lat.png)
* [Southern Hemisphere - Temperature (F) vs. Latitude](saved_figures/southern_hem_maxtemp_vs_lat.png)
* [Northern Hemisphere - Humidity (%) vs. Latitude](saved_figures/northern_hem_humidity_vs_lat.png)
* [Southern Hemisphere - Humidity (%) vs. Latitude](saved_figures/southern_hem_humidity_vs_lat.png)
* [Northern Hemisphere - Cloudiness (%) vs. Latitude](saved_figures/northern_hem_cloudiness_vs_lat.png)
* [Southern Hemisphere - Cloudiness (%) vs. Latitude](saved_figures/southern_hem_cloudiness_vs_lat.png)
* [Northern Hemisphere - Wind Speed (mph) vs. Latitude](saved_figures/northern_hem_windspeed_vs_lat.png)
* [Southern Hemisphere - Wind Speed (mph) vs. Latitude](saved_figures/southern_hem_windspeed_vs_lat.png)

### Dataframe
The Pandas libray was utilized to create dataframes to hold the data of the 500+ cities and saved as a CSV file. 
* [Weather Data](Weather_Py/clean_city_data.csv)


### Part II - VacationPy

Now let's use your skills in working with weather data to plan future vacations. Use jupyter-gmaps and the Google Places API for this part of the assignment.

* **Note:** if you having trouble displaying the maps try running `jupyter nbextension enable --py gmaps` in your environment and retry.

* Create a heat map that displays the humidity for every city from the part I of the homework.

  ![heatmap](trilogy_images/heatmap.png)

* Narrow down the DataFrame to find your ideal weather condition. For example:

  * A max temperature lower than 80 degrees but higher than 70.

  * Wind speed less than 10 mph.

  * Zero cloudiness.

  * Drop any rows that don't contain all three conditions. You want to be sure the weather is ideal.

  * **Note:** Feel free to adjust to your specifications but be sure to limit the number of rows returned by your API requests to a reasonable number.

* Using Google Places API to find the first hotel for each city located within 5000 meters of your coordinates.

* Plot the hotels on top of the humidity heatmap with each pin containing the **Hotel Name**, **City**, and **Country**.

  ![hotel map](trilogy_images/hotel_map.png)

As final considerations:

* Create a new GitHub repository for this project called `API-Challenge` (note the kebab-case). **Do not add to an existing repo**
* You must complete your analysis using a Jupyter notebook.
* You must use the Matplotlib or Pandas plotting libraries.
* For Part I, you must include a written description of three observable trends based on the data.
* You must use proper labeling of your plots, including aspects like: Plot Titles (with date of analysis) and Axes Labels.
* For max intensity in the heat map, try setting it to the highest humidity found in the data set.
