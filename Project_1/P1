---
  title: Project 1
---
## Spatialite Queries and 3D Mapping

 Joshua SCHAFERBIEN   GES 486 10/8/18

## Data:

To begin with, my project used different datasets including the the real_property data given to us by Professor Dillion. He(you) could of attained this thorough data by either getting from a previous job or sifting through census block datasets.
Most of the data used within this project was supplied by the open data portal for Baltimore city.(https://data.baltimorecity.gov/) I downloaded the city boundary line, and neighborhood shapefile. The building heights and geometries were from open Baltimorecity.gov even though it is mostly scrubbed the attribute table shows heights of the buildings in 2017 and shape length, area and polygons of the building footprints. (https://data.baltimorecity.gov/Geographic/Building-Footprint-Shape/deus-s85f).

## Projections/coordinate system:

For this project I used the North_America_Albers_Equal_Area_Conic EPSG: 102008 for the data frame and for the projection
CRS
EPSG:2893 - NAD83(HARN) / Maryland (ftUS) - Projected



## Tools used:
In QGIS v3.2 in order to create the hexagon layout of Baltimore City. First had to use the create grid tool by using the layers extent to make a hexagon grid. Next I used the clip tool to clip the hexagon grid to the city line boundary. With the Baltimore building shapefile I used the convert polygons to centroids tool in order to convert the building shapefile to a point layer. This resulted me using the new point layer to later use the count points within polygons tool. The tool used the new polygons such as the hexagon grid and the centroids in order to give me a map interpreting the count of centroids within the hexagon grid giving me a heat map of densely populated building areas within Baltimore City.

![](https://i.imgur.com/nBKcMTQ.png)

## Spatialite Database Querying:

For the querying part of the project I used the database in QGIS to query what taxed land in Baltimore City is taxed over $500000 with its land use as commercial. I used to compare this query with building heights to see if thee was a correlation between larger building heights with larger taxed land in Baltimore City. In a later query I located the buildings that were over 100ft and some of the buildings were built on the top taxed land.

![](https://i.imgur.com/OwsMy8X.gif)

## 2.5D:

Working in QGIS v3.2 I tried to make a 3D map of the buildings within the Baltimore City Inner Harbor region, however with some projections errors or drawing errors I could not get it to work. So I end up making a small test of the symbology of the buildings, called 2.5D, Picture Below.

![](https://i.imgur.com/VTM1EUF.jpg)

## 3D Mapping:

Using Arcscene from the ESRI Desktop Suite I was able to create a 3D map of the Buildings near the Inner Harbor of Baltimore, Maryland. The real_property data was used as the canvas to compare the building height extrusions and the highest City Taxed Parcels.

![](https://i.imgur.com/WXVxTQw.gif)

![](https://i.imgur.com/kWdo2yA.gif)
