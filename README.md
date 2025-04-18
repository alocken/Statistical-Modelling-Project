# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
Connecting to and exploring new APIs to gather and analyze data to determine locations of bike sharing stations and points on interest (POI) within the radius of those stations. The bike sharing location selected was AlGira in the city of Almeirim and the points of interest selected were cafes and bars. The end goal of this project was to determine the correlation between the bike stations within the selected city and location of corresponding cafes/bars in proximity to those bike stations. The final goal was to then generate a regression model that reflected the data obtained and determining statistical significance of the variables through model outputs. 

## Process
Step 1: Request AlGira Almeirim bike stations data through a call to the CityBikes API. Explored data and used API to call latitude and longitude of bike station locations as well as number of bikes for each location. 

Step 2: Connected to both the Foursquare and Yelp APIs to retrieve points of interest (POIs) aligned to the latitude and longitude from AlGira Almeirim location selected in Step 1. Selected both cafes and bars as designated POIs and called each API to retrieve the information. Determined that Foursquare provided best coverage for the ask when compared to Yelp.

Step 3: Joined data from Step 1 and 2 to support development of a data frame to generate a data visualization to join together and visualize the data findings. Opted for a scatter plot visualization that leveraged the latitude and longitude ranges from Step 1 (also used in Step 2 to find POIs within the same proximity) as axis and categories (cafes, bars) as the data points on the plot. Higher density of POIs were observed in specific ranges of the plot. 

Step 4: Utilized the data and observations from Step 1 through 3 to develop a regression model that sought to determine the correlation between the location of a bike station and cafes/bars POIs.  

## Results

### Comparative quality of API coverage  

Coverage was defined by number of points of interest (POI) returned within the request and the category lists associated with each POI returned being more comprehensive in description. 
Foursquare returned more complete information that provided better coverage when returning data associated with bars and cafes. When exploring the top 10 restaurants according to their rating, Yelp provided more complete information providing better coverage as the data returned provided ratings where Foursquare data did not. 

### Results of regression model

The outputs of the model indicated model is capable of explaining 79.6% (R-squared value) of the patterns in the data. The p-value for the bike station count being .017 then further indicated the statistical significance and likelihood of potential correlation between the locations of bike stations and cafes/bars.

Additionally, the coefficient of bike station count to cafe/bars is 3.1943 indicating there is a positive correlation and for every bike station, the expectation would be to observe roughly three cafes/bars nearby. 

## Challenges 
Joining data was challenging as it required exploration to determine how to join/merge sets as well as to determine alignment in naming conventions. 
Building a regression model was a challenge as it required research to determine how to evaluate two sets of data to produce a comparative output. This took time and was a stretch as it required developing a grid and cells to evaluate locations of data and potential correlations. 


## Future Goals
I would like to explore filtering returned data further as it was unclear when filtering cafes/bars if some of the returned results were due to a cafe/bar being within a category or if this was in error. Due to limitations on time, there was not an opportunity to explore this further to confirm or remove. Also, exploring as well as expanding the parameters of the data returned would be helpful given the size of the location chosen being relatively small so either expanding the parameters to include a larger geographic areas or selecting a new destination to repeat the exercise would be beneficial. I would also like to determine if there is another method for building a regression model that utilizes an alternate approach to the grid that could still return valuable results that could be analyzed. 
