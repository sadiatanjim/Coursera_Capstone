## Data

Say, for our problem, a business owner wants to open a new **Restaurant** in the city of **Toronto**. 

In order to decide on a suitable location for a particular business, might take help from a variety of data sources. Historical trends in that area, existing businesses, places or venues around that area - might provide us valueable insights to answer our questions.

We use two data sources for this task. Firstly, we need to have a list of probable neighborhoods around the city of Toronto. In order to obtain a list of neighborhoods around the city of Toronto, we scraped a [Wikipedia Table](https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M) to collect information i.e. Names of different neighborhoods in Toronto, their Postal Codes and Co-ordinates (Latitudes & Longitudes etc.

An example of a couple of records from the scraped table is as follows: 

![Neighborhood Dataframe from Webscraping](https://raw.githubusercontent.com/sadiatanjim/Coursera_Capstone/master/Report/neighborhood_df.jpg)

The second, and most important source of data is the Foursquare API. We shall utilize the neighborhood-wise information obtained from the wikipedia table to make calls to the Foursquare API to collect information about the most popular venues in those locations. Foursquare also categorizes its venues into some categories which might be helpful for our task. We utilize the foursquare API to extract the following data fields for each venue - 
* Venue Name
* Neighborhood
* Venue Location (Latitude &  Longitude)
* Venue Type/Category

An example of the information obtained from the Foursquare API, after some preprocessing is shown as follows:

![Venue DataFrame from Foursquare](https://raw.githubusercontent.com/sadiatanjim/Coursera_Capstone/master/Report/venue_df.jpg)
