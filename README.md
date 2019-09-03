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
I started with **k-means** clustering in order to create a map for general exploration. This also helped validate my features since the clusters tended to be geographically nearby, suburbs clustered together and Chicago and NYC neighborhoods tended to get separated into different clusters. </br>
<img src="https://github.com/hasgrig/Coursera_Capstone/blob/master/sample_screenshots/Chi_clust.JPG" alt="Chicago clustered" width="400" height="400">
<img src="https://github.com/hasgrig/Coursera_Capstone/blob/master/sample_screenshots/NYC_clust.JPG" alt="NYC clustered" width="400" height="400">
While clustering provides a fun tool for exploring the two cities in general and globally comparing the neighborhoods between them, it is not a good recommender. For this reason I used **cosine similarity** and wrote a function that maps most similar neighborhoods to a neighborhood of your choice. 
<figure>
  <img src="https://github.com/hasgrig/Coursera_Capstone/blob/master/sample_screenshots/soho_chi.JPG" alt="Soho" width = "400" height = "400">
  <figcaption>Recommendations in Chicago if you like SoHo in NYC</figcaption>
</figure>
<figure>
  <img src="https://github.com/hasgrig/Coursera_Capstone/blob/master/sample_screenshots/wicker_nyc.JPG" alt="Wicker" width = "400" height = "400">
  <figcaption>Recommendations in New York if you like Wicker Park in Chicago</figcaption>
</figure>
### Discussion
Because the purpose of this tool is recommending neighborhoods further analysis could be done to provide explanations for the recommendations. Right now, each recommendation comes with a similarity score. However, given the simple design of the features, one could provide a visualization further breaking apart the similarity in categories. Example venues from the most influential features could also be a good idea. 
### Final Notes
Because this tool is meant to be interacted with I highly recommend looking into the codde and trying out some neighborhoods that you're familiar with. </br>
**Coursera_Capstone.pdf** is the formal report for the project and includes more details on the methodologies and the results. </br>
**Neighborhood-Recommender.ipynb** is the full project from data scraping to preprocessing to results. </br>
**.csv files** are some of the dataframes set up in the code that I saved for ease of use </br>
The other .ipynb files are smaller projects completed during the capstone course. 
