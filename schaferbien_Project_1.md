# Project 1  Spatialite Queries and 3D Mapping

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

https://i.imgur.com/nBKcMTQ.png

## Spatialite Database Querying
