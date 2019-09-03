# Comparing Neighborhoods between Chicago and New York City 
## IBM Data Science Professional Certificate </br> Capstone Project
### Introduction
Most big enough cities have similar sets of neighborhoods; the homey ones, the ones great for night life and entertainment, the ones with the most museums, etc. In my experience, it takes some time before you figure out what your favorite ones are when moving into a new city. With this in mind, I explored neighborhoods in Chicago and New York City. The main goal was to make a recommender system that suggests neighborhoods to explore based on a favorite neighborhood in one of the cities. 
### Data
I scraped the list of neighborhoods for Chicago and NYC from Wikipedia. I used **geopy** in order to get the latitude and longitude of the neighborhoods. The data needed cleaning because of incorrect locations returned by geopy and improperly named neighborhoods. I ended up with 225 neighborhoods in Chicago and 303 in NYC. 
<img src="https://github.com/hasgrig/Coursera_Capstone/blob/master/sample_screenshots/Chicago.JPG" alt="chicago" width="400" height="400">
<img src="https://github.com/hasgrig/Coursera_Capstone/blob/master/sample_screenshots/NYC.JPG" alt="NYC" width="400" height="400">
