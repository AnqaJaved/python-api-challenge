# Python API Challenge: WeatherPy and VacationPy

## by: Anqa Javed

This project explores the weather data from over 500 cities around the world, using the OpenWeatherMap API to gather weather data, and visualizing the data through plots and interactive maps. Additionally, it uses the Geoapify API to plan vacations based on ideal weather conditions. The project is split into two parts:

- **Part 1: WeatherPy**: Visualizing weather data from cities based on latitude.
- **Part 2: VacationPy**: Using weather data to plan ideal vacations and finding hotels using the Geoapify API.

### Table of Contents

- [Part 1: WeatherPy](#part-1-weatherpy)
  - [Create Plots to Showcase the Relationship Between Weather Variables and Latitude](#create-plots-to-showcase-the-relationship-between-weather-variables-and-latitude)
  - [Compute Linear Regression for Each Relationship](#compute-linear-regression-for-each-relationship)
- [Part 2: VacationPy](#part-2-vacationpy)
  - [Create a Map Showing Points for Each City](#create-a-map-showing-points-for-each-city)
  - [Narrowing Down the Data for Ideal Weather Conditions](#narrowing-down-the-data-for-ideal-weather-conditions)
  - [Finding Hotels Near the Selected Cities](#finding-hotels-near-the-selected-cities)
  - [Displaying Hotel and Country Information on the Map](#displaying-hotel-and-country-information-on-the-map)
- [Conclusion](#conclusion)

## Part 1: WeatherPy

In **Part 1**,
i visualized the weather data of over 500 cities to explore the relationship between various weather variables and latitude. The steps involved using the **OpenWeatherMap API** to collect data, and creating plots for the following relationships:

### Create Plots to Showcase the Relationship Between Weather Variables and Latitude

- **Latitude vs. Temperature**
- **Latitude vs. Humidity**
- **Latitude vs. Cloudiness**
- **Latitude vs. Wind Speed**

These plots were generated using Python's **Matplotlib** and **hvplot** libraries to create clear, informative scatter plots.

### Compute Linear Regression for Each Relationship

For each weather relationship mentioned above, i calculated linear regression for both the **Northern Hemisphere** and **Southern Hemisphere**.

- **Northern Hemisphere:**
  - Temperature vs. Latitude
  - Humidity vs. Latitude
  - Cloudiness vs. Latitude
  - Wind Speed vs. Latitude
- **Southern Hemisphere:**
  - Temperature vs. Latitude
  - Humidity vs. Latitude
  - Cloudiness vs. Latitude
  - Wind Speed vs. Latitude

Linear regression models were created to analyze and describe the relationship between weather variables and latitude. The regression lines, formulas, and R² values were displayed on the plots.

## Part 2: VacationPy

In **Part 2**,i used the **Geoapify API** and **geoviews** to plan ideal vacations based on weather data. The steps involved:

### Create a Map Showing Points for Each City

i created an interactive map that displays a point for every city from the `city_data_df` DataFrame, with the size of the point corresponding to the humidity in each city. This map was built using the **hvplot** library.

### Narrowing Down the Data for Ideal Weather Conditions

i narrowed down the cities to match certain ideal weather conditions:
- Max temperature between 20°C and 25°C
- Humidity between 30% and 50%
- Wind speed less than 10 m/s

This filtered data was used for vacation planning.

### Finding Hotels Near the Selected Cities

For each city in the filtered DataFrame (`hotel_df`), i used the **Geoapify API** to find the first hotel located within a 10,000-meter radius of the city's coordinates. The hotel name was added to the `hotel_df` DataFrame.

### Displaying Hotel and Country Information on the Map

i updated the map to display additional information on hover, including the city name, country, and the nearest hotel found using the Geoapify API.

## Conclusion

The project demonstrates the ability to retrieve and analyze weather data from multiple cities worldwide using APIs, visualize that data, and plan vacations based on specific weather conditions. The data was gathered using the **OpenWeatherMap API** and visualized using **Matplotlib** and **hvplot**. Hotel search functionality was implemented using the **Geoapify API** to find accommodations near cities that matched the desired weather conditions.

## Repository Structure

- **api_keys.py**: Contains the API keys for the OpenWeatherMap and Geoapify APIs (not shared in this repository for security reasons).
- **WeatherPy.ipynb**: The Jupyter notebook that handles weather data collection, analysis, and plotting.
- **VacationPy.ipynb**: The Jupyter notebook that handles vacation planning using the weather data and Geoapify API for hotel searches.
- **output_data/cities.csv**: The CSV file containing the city data for weather analysis.
- **.gitignore**: Prevents the `api_keys.py` file from being uploaded to GitHub.

## Requirements

To run this project, you'll need the following Python libraries:

- `requests`
- `pandas`
- `hvplot`
- `geoviews`
- `geopandas`
- `matplotlib`
- `scipy`
