# Special Works - Project 5 - Minimum Driving Distance

[![Introduction Video](http://img.youtube.com/vi/-3klc9kqb8Q/0.jpg)](https://youtu.be/-3klc9kqb8Q "Special Works 5")

**Scenario**

A client that has presented you with a CSV of coordinates (addresses that have already been geocoded, but are anonymized) and wants to know the shortest driving distance (in miles) between each pair of points (i.e., create a minimum driving distance matrix). 
They want to know if the process can be automated and need an explanation of the procedure for their thesis. 

The CSV, [advgis_mdd.csv](./advgis_mdd.csv), is provided here as well as on ArcGIS Online ([advgis_mdd.csv](https://wm-gis.maps.arcgis.com/home/item.html?id=85ef209e191b41419ca555492c60935a)).

**Basic Level**

Create a minimum driving distance matrix between each set of points given.
Be sure to maintain the original IDs that are associated with each of the locations.

Export your solution as a CSV file.

**Intermediate Level**

When determining driving distances, sometimes it is helpful to have some basic spatial statistics for comparison.

Perform two point pattern analyses.

1. [Centrography](https://mgimond.github.io/Spatial/chp11-0.html#centrography) if link doesn't work here is the url to copy: https://mgimond.github.io/Spatial/chp11_0.html#centrography
    * Calculate the mean center, standard distance and standard deviational ellipse of the point locations used for computing the minimum driving distance
    * Create a figure that overlays these features with the original point locations
2. [Distance based analysis](https://mgimond.github.io/Spatial/chp11-0.html#distance-based-analysis)
    * Compute the average nearest neighbor (ANN) in miles using the minimum driving distances found in the Basic Level analysis

**Advanced Level** (_GIS 520_)

Another important statistic for analyzing driving routes among locations is identifying clusters.
One way to do this is using [K and L functions](https://mgimond.github.io/Spatial/chp11-0.html#k-and-l-functions).

* Perform a K-function analysis of given locations using both driving distances and circular radii.
* Plot the calculated K values against distance. Compare the Ks from the two distance methods.
* Compare the calculated K values against the expected K value from a completely spatial random (CSR) / independent random process (IRP) distribution.

### GitHub Issue
[Special Works 5 (issue)](https://github.com/cga-wm/advgis-echo/issues/6)

### Shared Google Doc
[Special Works 5 (.gdoc)](https://docs.google.com/document/d/13WM2O0EUuvhKQrr0pYtatrSYoXHJNr2ITgqN0KYDg6g/edit?usp=sharing)
