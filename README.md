# python_api_challenge
In this challenge, I analyzed the relationship between various weather parameters and geographical latitude. Initially, I set up my environment by installing and importing necessary libraries like ‘matplotlib’, ‘scipy’, and ‘citipy’. I then obtained my API key for OpenWeatherMap from the ‘api_keys’ module.

The next step was to generate a list of random geographic coordinates. I utilized numpy to produce 1500 random latitudes and longitudes. By zipping these values, I formed coordinate pairs, and with the help of the ‘citipy’ library, I mapped each of these coordinates to its nearest city. This resulted in a diverse list of city names spread across the globe.

After establishing the list of cities, I proceeded to fetch weather data for each city from OpenWeatherMap. To keep track of my data fetching process, I employed counters and printed logs for every 50th record. The main data retrieval was achieved using the requests library, where I sent an API request for each city in the list and extracted essential details like latitude, longitude, temperature, humidity, cloudiness, wind speed, and more.

Having obtained the weather data, I transformed it into a Pandas DataFrame, saved it as a CSV file, and then read it back for further processing. With this data on hand, I visualized the relationship between latitude and various weather parameters using scatter plots. Four plots were created, showcasing the relationship of latitude with max temperature, humidity, cloudiness, and wind speed, respectively.

The final task was to calculate and visualize the linear regression for each relationship, separating the data between the Northern and Southern Hemispheres. For this, I utilized the ‘linregress’ function from the ‘scipy.stats’ library to compute the linear regression values. A function named ‘plot_linear_regression’ was crafted, which not only plotted scatter points but also superimposed the regression line on top, along with its equation. This process was repeated for each of the weather parameters against latitude, and both the Northern and Southern Hemispheres were analyzed separately. All the plots were saved as PNG files for easy reference.
