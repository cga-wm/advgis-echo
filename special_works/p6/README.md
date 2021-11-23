# Special Works - Project 6 - Table Queries and Joins
[Introduction (.mp3)](https://drive.google.com/file/d/1V_3G9Arkj145V_XmA4AeztV6wq_Ka52j/view)

**Scenario**

A client has provided us with the following CSV file:

* Unprovoked shark encounters in NC and SC from 1995 to 2019 (142 incidents retrieved from the [Global Shark Attack File](http://www.sharkattackfile.net/))
    * [advgis_sharks.csv](./advgis_sharks.csv)
    * [advgis_sharks.csv (ArcGIS Online)](https://wm-gis.maps.arcgis.com/home/item.html?id=408743bcd58344609c792172874629ca)

The client has provided two extra bits of information to their dataset:

* Longitude and Latitude: geocoded based on the best information derived from the datasets and their associated PDF files
* NAME_WEATHER: the name of the closest NOAA weather station based on a proximity analysis (e.g., find nearest)

**Basic Level**

The client has asked you to add to this file the daily rainfall and air temperature associated with each attack (i.e., match the date and location).

Daily weather can be downloaded from the internet using NOAA's [Daily Observational Data Map](https://gis.ncdc.noaa.gov/maps/ncei/cdo/daily).
For more information on how to download these data, see [How to Get Daily Weather Data (ArcGIS Notebook)](https://wm-gis.maps.arcgis.com/home/item.html?id=fcf1b08b9ced4dde955067b697d251f3#overview).

Find, download and join the weather data to get the daily rainfall (precipitation) and the daily maximum/minimum air temperature.
The output should have all the columns of the original CSV file plus the corresponding daily weather.

_Note: the shark attack dataset is created and maintained by registered users; therefore, you may encounter some errors in the dataset._

**Intermediate Level**

* Identify and categorize any rows in the shark attack dataset with errors in the data record.
* How many shark attack incidents did not have a match for daily weather from the table join performed in the Basic Level analysis?
* Propose values for any missing entries.

**Advanced Level** (_GIS 520_)

Design a model to predict the likelihood of a shark encounter (or intensity of shark encounters) using any variable(s) in the joined table as a predictor(s).


### GitHub Issue 
[Special Works 6 (issue)](https://github.com/cga-wm/advgis-echo/issues/7)

### Shared Google Doc
[Special Works 6 (.gdoc)](https://docs.google.com/document/d/1XmHMNj63MSWtijPL-JuGfpmVLshG_Gd7fg2njE9t-KQ/edit?usp=sharing)
