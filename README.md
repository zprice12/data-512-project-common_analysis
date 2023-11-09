# Data 512 - Project - Common Analysis
## Project Goal
The goal of this project is to investigate forest fires near Kingman, Arizona by developing a smoke impact metric, predicting this metric through 2049, and creating informative visualizations.
## Licenses and Links
USGS Wildfire Data -  
https://www.sciencebase.gov/catalog/item/61aa537dd34eb622f699df81
EPA AQI Information -  
https://www.airnow.gov/sites/default/files/2020-05/aqi-technical-assistance-document-sept2018.pdf  
Pyproj Documentation -  
https://pyproj4.github.io/pyproj/stable/index.html  
Geojson Documentation -  
https://pypi.org/project/geojson/ 
Code License -  
https://creativecommons.org/licenses/by/4.0/  
EPSG:4326 Information -  
https://epsg.io/4326 
US EPA AQI Documentation -  
https://aqs.epa.gov/aqsweb/documents/data_api.html  
US EPA FAQ -  
https://www.epa.gov/outdoor-air-quality-data/frequent-questions-about-airdata
FIPS Information -  
https://www.census.gov/library/reference/code-lists/ansi.html
## Data Files
### state_pops.csv
This data file includes census data with each state's population. It includes a state field with the name of the state and a population field with the population of the state.
### us_regions.csv
This data file includes data on each state's region. It includes a DIVISION field with the regional division of the state and a STATE field with the name of the state.
### us_cities_by_state_SEPT.2023.csv
This data file includes the articles we wish to investigate in this project. It includes a state field with the name of the state, a page_title field with the name of the article, and a url field with a url to the article.
### wp_scored_city_articles_by_state.csv
This data file includes information on article quality for each of the articles. It includes a state field with the name of the state, a regional_division field with the region that the article belongs to, a population field with the population of the state, an article_title field with the title of the article, a revision_id field with the revision version of the article, and an article_quality field with the ORES score for the article.
## Special Considerations
Both API requests take several hours to complete, so budget time accordingly and save upon completion.
## Research Implications
Throughout this process of completing this project, I learned several things about bias, data science, and Wikipedia article grading. First, I learned to not underestimate the duration of an API query. I spent most of the homework simply waiting for the two queries to run; I will start these assignments earlier in the future. Second, I learned that it's important to investigate anomalies in data. This allowed me to improve matching when merging the population data. Lastly, I learned that bias could exist throughout any data. It’s important to understand where the data comes from and what lies within it in order to combat bias. I found several interesting things throughout these investigations. First, Vermont, North Dakota, and Maine are the three most covered states per capita. In addition, Vermont, Wyoming, and South Dakota are the three states with the highest quality articles per capita. Lastly, the West North Central region has the highest coverage and highest quality coverage per capita out of all regions. There were a few things that surprised me about my findings. First, I expected tourist states like Florida and California to receive lots of high quality coverage per capita. However, these two states finished bottom 10 in coverage and high quality coverage. Also, I thought New England would get higher quality coverage due to its number of universities; but, it finished low in high quality coverage. Finally, I did not expect West North Central to be first in coverage and high quality coverage due to its lack of tourism.
### What biases did you expect to find in the data (before you started working with it), and why?
I expected states with large amounts of tourism to receive more high quality coverage. I assumed this because these highly visited cities might put more effort into their Wikipedia pages. However, this did not appear to be the case after looking through the results. Furthermore, I expected older cities to earn higher reviews because their Wikipedia pages should have been around for longer; thus, there’s been more time to perfect them.
### What (potential) sources of bias did you discover in the course of your data processing and analysis?
I discovered multiple potential sources of bias throughout data processing and analysis. First, the csv with article names had many repeat articles that could misguide analysis if not handled correctly. Second, the article names did not match perfectly for certain states when merging with the census data. Specifically, states with spaces would not merge correctly and Georgia was oddly formatted. Lastly, there were no articles on Nebraska or Connecticut; thus, these states are not even represented in the analysis individually and regionally.
### What might your results suggest about (English) Wikipedia as a data source?
My results suggest that using Wikipedia as a data source should be done with careful consideration. We can’t simply trust Wikipedia, but it is still a great tool for gathering vast information. One must understand the data fully that they are gathering from Wikipedia to avoid potential sources of bias and account for them. Even then, it’s helpful to check with other known data sources, if available, to corroborate information from Wikipedia. 

