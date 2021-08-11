# Special Works - Project 3 - Watershed Delineation

[![Introduction Video](http://img.youtube.com/vi/63zNerTJgv4/0.jpg)](https://youtu.be/63zNerTJgv4 "Special Works 3")

**Scenario:**  

It is grape vine sowing season in Napa Valley California for the coming year's vineyards and one of the deciding factors in a successful harvest is the availability of water. 
Irrigation plays an important role for this crop and an agricultural firm has asked you to calculate the watershed area (i.e., the area of land that collects rainwater) that feeds their irrigation pump located on Salvador Creek not far from Vintage High School (lat/lon: +38.3326,-122.3107). 

Hear Professor Davis explain more about this project [here (.mp3)](https://drive.google.com/file/d/1VooohsXYCGsWZLOavzFfbGd9HA06H3hF/view).

**Basic Level** 

Follow the outline of watershed delineation process to determine the area of land that drains through the Salvador Creek at (or near) the location of the client's irrigation pump.

1.  Find 10 m elevation data for the Napa, CA region (make sure you know what resampling technique to use)
2.  Follow the summarized steps below to define the watershed that has an outlet located at (or near) their irrigation station
3.  Calculate the area of that watershed
4.  Keep track of all the steps that you take, all the geoprocessing tools you use, all the research/reference articles you utilize, and all collaborations you are involved in (and the time you spent doing them)

**Intermediate Level**

Watershed delineation is a multi-step process and the client has expressed interest, if this project is successful, for you to delineate several more watersheds throughout the region. 
Knowing that you will have to repeat this process, you decide to create a model of the procedure so you don't forget any steps and simplify the repeatability.

Produce either a graphical model (e.g., ModelBuilder in ArcGIS or Graphical Modeler in QGIS) or programmatic model (e.g., ArcGIS Notebook) that represents the procedure for watershed delineation and calculate the area of the watershed around Salvador Creek for the client.

**Advanced Level** (_GIS 520_)

The client's pump station is nearing its end-of-life and the client has asked for an analysis of alternative pump station locations.

Provide three alternatives within a 10-mile radius of the existing pump house.
The new basin should be within 20% of the original basin size.
Be sure to justify your choices.

---

**Outline of Watershed Delineation Procedure**

1.  Fill your holes.

    Pre-process the digital elevation raster to ensure that there are no "holes" in the landscape caused by satellite sensor error or processing artifacts from the data provider, which would result in an artificial pond or lake forming where there isn't one.
2.  Water always flows downhill. 
    
    In a raster format, rainwater that falls on a pixel will travel to one of its eight neighbors based on which one has the lowest relative elevation (i.e., downhill). 
    Determine the over-land [flow direction](https://pro.arcgis.com/en/pro-app/latest/tool-reference/spatial-analyst/how-flow-direction-works.htm) based on the filled digital elevation model.
3.  The snowball effect.

    In raster format, each pixel drains to its neighbor with the steepest drop in elevation. 
    As water travels downhill, it follows the paths of others and picks up water drops along the way. 
    This represents a cumulating effect as water passes over the pixels of a given surface raster. 
    The larger the accumulated water, the more likely it will develop into a river or stream when it rains.
    Determine the [flow accumulation](https://pro.arcgis.com/en/pro-app/latest/tool-reference/spatial-analyst/how-flow-accumulation-works.htm) based on the flow direction dataset.
4.  Every watershed is defined by its outlet. 

    Pick a point (any point) in the flow accumulation raster and each point has the associated pixels scattered over the landscape where the rainwater that landed there ended up flowing over that point.
    This means that every pixel in the flow accumulation layer has an associated drainage area (i.e., watershed) associated with it.
    The larger the flow accumulation value, the larger the associated drainage area.
    Find the pour point (i.e., the pixel in your flow accumulation that has the highest flow accumulation value proximal to your outlet location) that is best for the pump station.
5.  Delineate the watershed based on the pour point and flow direction data.
6.  Calculate the area of the watershed you found.
    
    TMTOWTDI (there's more than one way to do it).

### GitHub Issue
[Special Works 3 (issue)](https://github.com/cga-wm/advgis-echo/issues/4)

### Shared Google Doc 
[Special Works 3 (.gdoc)](https://docs.google.com/document/d/1anrl_3Zeow7ZUGmfeRw-2RWirkCwPzsc5_QizuFcflA/edit?usp=sharing)
