# web-scraping-challenge:

Build a web application 'Mission to Mars' of

1. scraping  various websites

  - [NASA Mars News Site](https://mars.nasa.gov/news/)

  - [JPL Featured Space Image](https://www.jpl.nasa.gov/spaceimages/?search=&category=Mars)

  - [Mars Facts webpage](https://space-facts.com/mars/)

  - [USGS Astrogeology site](https://astrogeology.usgs.gov/search/results?q=hemisphere+enhanced&k1=target&v1=Mars)

2. storing the data into MongoDB

3. displaying the information in a single HTML page

## Step 1 - Scraping

* mission_to_mars.ipynb, mission_to_mars.py

#### NASA Mars News

* url= (https://mars.nasa.gov/news/)

* Collect the latest News Title and Paragraph Text

#### JPL Mars Space Images - Featured Image

* url= (https://www.jpl.nasa.gov/spaceimages/?search=&category=Mars)

* Find the image url for the current Featured Mars Image

#### Mars Facts

* url= (https://space-facts.com/mars/)

* Scrape the table containing facts about the planet including Diameter, Mass, etc

#### Mars Hemispheres

* url= (https://astrogeology.usgs.gov/search/results?q=hemisphere+enhanced&k1=target&v1=Mars)

* Obtain high resolution image url and title for each of Mar's hemispheres


## Step 2 - MongoDB and Flask Application

* app.py

  - route `/scrape` : import `scrape_mars.py` script and call `scrape` function to scrape all the mars data, followed by storing the data in MongoDB

  - rount '/' : query the Mongo database and pass the mars data into index.html by rendering

* templates/index.html : display the passed data.
