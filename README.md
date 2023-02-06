# premier-league-map
mapping the nationalities of PL players

## Plan
The plan is to create interactive and/or snapshot maps of the nationalities of players in England's Premier League. Given taht the Premier League is recognized as one of the top leagues in the world for football players, it draws players from all over the globe. It would be interesting to visualize where these players come from and identify if any trends change over time. I also want to play with the geospatial population density maps - this could be done by seeing what towns players come from in a country. 

## Data
Going to start with getting data from FBRef, since it can be easily downloaded as CSV files instead of web scraping. 

## Visualization
Several options ranging in ease-of-use and customization. Options include geopandas, pydeck, kepler.gl, pygal. Going to try starting with geopandas for simplicity.


### Day 1

FBRef was the first website I found which had the player nationality data. It had the nation, number of players, cumulative number of minutes by those players, and player names (which was capped at around 10 for countries with 10+ players). There were options to download Excel files, convert directly to CSV formatted text on the webpage, or get a link to the webpage table. 

To start, I downloaded an Excel file and loaded it into a pandas Dataframe. It worked, but the formatting of symbols of the names was odd. I copy and pasted the CSV data into a text editor and opened that as a Dataframe, which worked well. So I'll quickly copy and paste ~10 years of data into CSV files and load them. I could make a script to scrape the webpages, helped with the link to the table, but one thing I have learned is that automating that process will take me far longer than copy pasting for 2 minutes, and I only need a little bit of data to start. 

The CSV files don't need much cleaning, primarily reformatting and replacing NaNs with 0s where appropriate. The data only looks to go back to 1992, which is when the Premier League started. Since it is not very historical and I have already manually collected over a dozen years, I'll copy the other files and skip the web scraping. Then I'll automate the cleaning of all the other files. 


