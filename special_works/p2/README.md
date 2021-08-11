# Special Works - Project 2 - Spatial Interpolation

[![Introduction Video](http://img.youtube.com/vi/McCre9FOjVs/0.jpg)](https://youtu.be/McCre9FOjVs "Special Works 2")

A client has asked you to reproduce eight figures they found &sect;6.4.1.1 in the dissertation, "Environmental Monitoring Through Wireless Sensor Networks" by T. Davis (2012). 

Listen to Dr. Davis talk about this project [here (.mp3)](https://drive.google.com/file/d/12vqrKze-92e7VQGlJSv-D_s0TpjJa8kC/view).

Figures 43 through 50 represent seasonal soil water potential (i.e., a measure of how dry the soil is---the more negative the measurement, the higher the potential, the drier the soil) from 25 sensors over a two-year period (2010--2012).
Table 19 shows the starting and ending dates for each of the seasons used in the analysis and Table 20 shows the sensor node identifying numbers (i.e., sensor node IDs) for the 25 sensors used in the analysis.

You are only provided with the monthly average soil water potential measurements for the 25 sensors listed in Table 20.
These data are available in the CSV file: [monthly_average_swp.csv](./monthly_average_swp.csv).
The data have been calculated and corrected such that the data are in units of kilo-Pascals (kPa) and missing values or erroneous measurements are given the value zero (0).
The header row of this CSV file contains the 25 node IDs.

To get the locations of each sensor, a GPS survey was conducted (see [old_node_gps_survey.txt](./old_node_gps_survey.txt)); however, the sensor nodes were identified using a different numbering system at the time of the GPS survey (old IDs).
Since then, the sensors have been re-numbered (new IDs).
You can find a table that pairs the old and new IDs (see [old-to-new-ids.tsv](./old-to-new-ids.tsv)).

**Basic Level**

Your task is to recreate these eight figures to show how water potential changes seasonally over a hillslope in a forested region.
Please try to match the symbology (see legend).
Be sure to read this section of the dissertation for more details.
Remember, you may employ any tools and techniques you want to arrive at the solution.
Keep track of your methods!

Based on the reading, it seems that the basemap around the point locations of the sensors was created using isolines of elevation (i.e., contour lines).
These data are not provided; therefore, you will need to find elevation data (e.g., a digital elevation model) for the study area and create isolines to highlight the intervals shown.

Next, rather than just show points, the data have been associated with a grid where each grid cell is a square that covers an area of approximately 1.5 square meters.
To create this regular grid of cells, the author likely employed the use of a fishnet and the "algorithm used to select grid cells located within 0.5 m of each node location" was likely a proximity analysis.

I could see selecting grid cells within a distance of node points and storing those cells in their own dataset, then doing an overlay analysis to associate node IDs with each cell.

**Intermediate Level**

Showing local changes within a few gridded areas is okay, but one nice thing (in general) about soil conditions, such water potential, is that they tend to be continuous across a given surface (or horizon).
Continuous variables can be estimated between known values because we know there has to be a smooth transition from one value to the next.

Create versions of the figures you created in the Basic Level where you estimate the values in between the sensors (i.e., [spatial interpolation](https://mgimond.github.io/Spatial/spatial-interpolation.html)) using one of the following [deterministic methods](https://mgimond.github.io/Spatial/spatial-interpolation.html#deterministic-approach-to-interpolation):

* proximity analysis (e.g., using Thiessen/voronoi polygons)
* inverse-distance weighted (IDW)

**Advanced Level** (_GIS 520_)

Create figures to compare the following spatial interpolation methods:

* proximity analysis (e.g., using Thiessen/voronoi polygons)
* inverse-distance weighted
* ordinary kriging

and answer the following questions:

* How does each method work?
* What are the strengths and weaknesses of each method?
* Which of these three methods do you think is the best at representing the missing values between sensor measurements?

### GitHub Discussion
[Special Works 2 (discussion board)](https://github.com/cga-wm/advgis-delta/discussions/8)

### Shared Google Doc
[Special Works 2 (.gdoc)](https://docs.google.com/document/d/1b0H8jBVHK8BOR0ewy-RggUPlpXgCi9b4F_hIriLJt9g/edit?usp=sharing)
