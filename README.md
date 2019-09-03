# Comparing Neighborhoods between Chicago and New York City 
## IBM Data Science Professional Certificate </br> Capstone Project
### Introduction
Most big enough cities have similar sets of neighborhoods; the homey ones, the ones great for night life and entertainment, the ones with the most museums, etc. In my experience, it takes some time before you figure out what your favorite ones are when moving into a new city. With this in mind, I explored neighborhoods in Chicago and New York City. The main goal was to make a recommender system that suggests neighborhoods to explore based on a favorite neighborhood in one of the cities. 
### Data and Feature Engineering
I scraped the list of neighborhoods for Chicago and NYC from Wikipedia. I used **geopy** in order to get the latitude and longitude of the neighborhoods. The data needed cleaning because of incorrect locations returned by geopy and improperly named neighborhoods. I ended up with 225 neighborhoods in Chicago and 303 in NYC. 
<img src="https://github.com/hasgrig/Coursera_Capstone/blob/master/sample_screenshots/Chicago.JPG" alt="chicago" width="400" height="400">
<img src="https://github.com/hasgrig/Coursera_Capstone/blob/master/sample_screenshots/NYC.JPG" alt="NYC" width="400" height="400">
I used **Foursquare API** to look up nearby venues for each neighborhood. After small modifications, the categories of venues became the features of each neighborhood with the value being number of venues in the category. Below are the top categories of venues. 
<img src="https://github.com/hasgrig/Coursera_Capstone/blob/master/sample_screenshots/TopVenues.JPG" alt="TopVenues">
### Methodology
I started with **k-means** clustering in order to create a map for general exploration. This also helped validate my features since the clusters tended to be geographically nearby, suburbs clustered together and Chicago and NYC neighborhoods tended to get separated into different clusters. 
<img src="https://github.com/hasgrig/Coursera_Capstone/blob/master/sample_screenshots/Chi_clust.JPG" alt="Chicago clustered" width="400" height="400">
<img src="https://github.com/hasgrig/Coursera_Capstone/blob/master/sample_screenshots/NYC_clust.JPG" alt="NYC clustered" width="400" height="400">


