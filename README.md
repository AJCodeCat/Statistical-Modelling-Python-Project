# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
My goals were to learn how to utilize APIs to gether data, parse JSON results so as to extract information, and clean and format it into useful dataframes for statistical analysis.

## Process
I began with performing GETs at City Bike's website to find bike-rental stations in Hamilton, Ontario. Finding 144, I then looked for family-friendly food establishments within 1000 meters of each station, settling on cafes, juice bars, ice-cream palours, and barbecue restaurants using API GETs at Yelp.com and Foursquare.com using the latitude and longitude coordinates from each bike station.

I used the results from each of the three websites to build a dataframe, and then merge the three dataframes into one using the coordinates as a key. There were many duplicates to be dropped, and a handful of five NaN missing values in the columns of the independent variables for my linear-regression model that I also dropped. 

## Results
Both point-of-interest websites offered many results, and they had many categories on which one could search. As a consumer, I would prefer Yelp for its ratings and review counts by which to evaluate if I want to visit a location, but as a data scientist, I value the precision of Foursquare's category codes so that you could know exactly you were (cafes serving coffee tea) and were not (VR cafes, internet cafes) searching for.

## Challenges 
Every step of the process involved major obstacles from parsing nested dictionaries and lists to get to the desired data points to cleaning the data of hidden missing values (less than 1% of the merged dataframe's rows) so that the regression would run. The biggest challenge was getting the list of coordinate points to successfully loop in requests, populate variables lists, and append to a dataframe. 

## Future Goals
There is a lot of different types of information available from Yelp and Foursquare. I would like to gather information on neighbourhoods without bike-rental stations and use them as a control group to try to find out what kinds of variables predict the existence and density of stations. 
