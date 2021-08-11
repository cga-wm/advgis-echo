# Special Works - Project 4 - Geocoding
[Introduction (.mp3)](https://drive.google.com/file/d/1LSRGm7Dio9Ci9-sZ8kOSK6csYohmXlaQ/view)

**Scenario**

A study by [Shalowitz et al. (2015)](https://doi.org/10.1016/j.ygyno.2015.04.025) suggests that a total of 36% of US counties are > 50 miles from the closest gynecologic oncologist, which results in approximately 9% of the US female population (14.8 million women) experiencing geographic barriers to high-quality gynecologic cancer treatment centers.
An independent research group is looking to see whether these numbers (percent counties and percent female population) have increased, decreased or stayed relatively the same since this paper was published.
One part of that work is getting a map of gynecologic oncologist treatment centers.

The only information you are given is a web address to:

* https://specialist.foundationforwomenscancer.org/

**Basic Level**

Get addresses from this website, geocode them (see introduction to geocoding below), and create a spatial point-data layer in GeoJSON file format.
Be sure to keep track of all methods, datasets, processes, tools, references, etc.

**Intermediate Level**

In addition to the Basic Level, also create a map of all the US counties that have a gynecologic oncologist office or care center.

**Advanced Level** (_GIS 520_)

See if you can provide an answer for the independent research group.

Are the numbers increasing, decreasing or staying about the same?

Also, estimate the number of women today that are experiencing a geographic barrier to high-quality gynecological cancer treatment centers.

---

**Introduction to Geocoding**

> "Geocoding is the process of transforming a description of a location&mdash;such as a pair of coordinates, an address, or a name of a place&mdash;to a location on the earth's surface. 
> You can geocode by providing one location description at a time to zoom to a location on a map or convert an entire table that can be used for spatial analysis."
>
> &mdash; from ["What is Geocoding"](https://pro.arcgis.com/en/pro-app/latest/help/data/geocoding/introduction-to-finding-places-on-a-map.htm) by Esri

The process of geocoding requires two things:

* a database of spatially defined addresses
* a geocoding algorithm

The creation of a database with spatially defined addresses takes a lot of effort (imagine taking a GPS unit and logging the coordinates and street address of every building in the United States).
Due to this, geocoding services tend to be non-free or are limited in the extent to which they work (e.g., state level or county level addresses only).
Further complicating things is the need for a good algorithm to match given addresses or coordinates to the closest or best match within the database.
Therefore, the quality of geocoders may vary widely.

With your ArcGIS account, you have access to the [ArcGIS World Geocoding Service](https://developers.arcgis.com/rest/geocode/api-reference/overview-world-geocoding-service.htm).
Please note that geocoding uses credits (40 credits per 1000 geocodes, see [here](https://doc.arcgis.com/en/arcgis-online/administer/credits.htm#ESRI_SECTION1_709121D2C7694DCAB9B8592F36F7A5BA)), so be sure to keep an eye on your individual credit allocations.

---

**Introduction to GeoJSON**

GeoJSON (Geospatial JavaScript Object Notation) is a plain text file format popular for representing data about geographic features, their properties, and their spatial extents.
GeoJSON uses a geographic coordinate reference system, [World Geodetic System 1984](https://epsg.io/4326), and units of decimal degrees.

References:

- https://macwright.com/2015/03/23/geojson-second-bite.html
- https://geojson.org/
- http://geojson.io/

### Davis's Geocoding Tutorials

**Kentucky Polling Stations**

Watch as Davis walks us through solving how to scrub a website for street addresses and programmatically retrieve geospatial coordinates for each address.

[![YouTube](http://img.youtube.com/vi/KcqWJdWsKlo/0.jpg)](https://youtu.be/KcqWJdWsKlo)

A copy of the Python script written in this tutorial is available [here (.py)](https://cga-wm.github.io/course/adv-gis/scripts/web_scrub.py).

**Gynecologic Oncologic Centers**

[YouTube Playlist](https://youtube.com/playlist?list=PLbIkNQKCuzMOSgHamvzS0KaEGaJ3goke1)

### GitHub Issue
[Special Works 4 (issue)](https://github.com/cga-wm/advgis-echo/issues/5)

### Shared Google Doc
[Special Works 4 (.gdoc)](https://docs.google.com/document/d/1lzVDGyGrbupVeWuNrusXDvVBA96kQxjzJvoPtz7ctew/edit?usp=sharing)
