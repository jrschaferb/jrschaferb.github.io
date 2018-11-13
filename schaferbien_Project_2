# Project 2  United states Wildfires

 Joshua SCHAFERBIEN   GES 486 11/11/18

## Data:

To begin with, my project used the United States Forest Service which contains the data from 1980-2016 Wildfires.

(https://wildfire.cr.usgs.gov/firehistory/data.html)

## Background
The united States Forest Service Provided us with information on the wildfires from 1980-2016. In the dataset there was 300,524 records of wildfires ranging from size class A to size class G.

#### Size Class of Fire

As to size of wildfire:

Class A - one-fourth acre or less;

Class B - more than one-fourth acre, but less than 10 acres;

Class C - 10 acres or more, but less than 100 acres;

Class D - 100 acres or more, but less than 300 acres;

Class E - 300 acres or more, but less than 1,000 acres;

Class F - 1,000 acres or more, but less than 5,000 acres;

Class G - 5,000 acres or more.

https://www.nwcg.gov/term/glossary/size-class-of-fire%C2%A0

## Process
I downloaded the data zip file from the United States Forest Service and stored the shapefiles in a SpatialLite database:

![database](https://user-images.githubusercontent.com/42807889/48357765-5496f780-e667-11e8-98b6-8cce33c20d6d.JPG)

I then sorted out my data into four equal time periods seen below. The select by expression tool was used to export the 4 newly selected features to layers.
![select by expression](https://user-images.githubusercontent.com/42807889/48358555-03880300-e669-11e8-87b3-e81b36fc26c8.JPG)

Once the layer was separated into 4 layers: 1981-1989,1990-1998,1999-2007,and 2008-2016 I used the select by attribute to pull out the sizeclass = 'G' since on the United States Forest Service Scale G sized wildfires are the biggest and over 5,000 acres wide.
![select by attribute](https://user-images.githubusercontent.com/42807889/48358517-f1a66000-e668-11e8-9ec9-33f8c2e4a1c8.JPG)



My project queried the years of 1981-2016 by sub dividing them into four 9 year periods:
#### 1981-1989
![1981_1989_class_g2](https://user-images.githubusercontent.com/42807889/48357560-e5b99e80-e666-11e8-905d-3c5e60b5ba92.jpg)
#### 1990-1998
![1990_1998_class_g2](https://user-images.githubusercontent.com/42807889/48357609-fd912280-e666-11e8-9140-3e28a821f391.jpg)
#### 1999-2007
![1999_2007_class_g2](https://user-images.githubusercontent.com/42807889/48357645-14d01000-e667-11e8-87c8-5dfbe796610b.jpg)
#### 2008-2016
![2008_2016_class_g2](https://user-images.githubusercontent.com/42807889/48357676-27e2e000-e667-11e8-9c37-a793c990ad0f.jpg)


## Projections/coordinate system:

For this project I used the
CRS
EPSG:4326 - WGS 84 - Geographic projection since it is of the United States as a default.




## Tools used:
In QGIS v3.2 in order to create the GIF containing the time series Giphy was used to edit the photos. Just as a Back up for the data I placed all my shapefiles into a database. The selection by expression and selection by attribute were the most used tools in this lab. I used QGIS python console to basically back track my process and create a code that selects out the size class G from each time period.


## Python Code for selecting out size G Wildfires
```Python
from PyQt5.QtGu import QColor

from PyQt5.QtCore import Qt

from qgis.utils import iface
#Adding Base Maps from Rest Service
qgis.utils.iface.addRasterLayer("http://server.arcgisonline.com/arcgis/rest/services/ESRI_Imagery_World_2D/MapServer?f=json&pretty=true","raster")
qgis.utils.iface.addRasterLayer("http://server.arcgisonline.com/ArcGIS/rest/services/Canvas/World_Light_Gray_Base/MapServer?f=json&pretty=true","raster")
iface.addVectorLayer('F:/UMBC/GES_486/486/project_2/Data/wf_usfs_1980_2016/wf_usfs_1980_2016.shp','wf_usfs_1980_2016','ogr')
# Querying for size class G
from qgis.core import *
#year 2008_2016
G2008 = QgsVectorLayer('F:/UMBC/GES_486/486/project_2/Data/database/2008_2016.sqlite','2008_2016','ogr')
QgsProject.instance().addMapLayer(G2008)
G2008.selectByExpression("sizeclass = 'G'")
QgsVectorFileWriter.writeAsVectorFormat(G2008, r'F:/UMBC/GES_486/486/project_2/Data/database/2008_2016py1.gpkg', 'utf-8', G2008.crs(),'GPKG', True)
iface.addVectorLayer('F:/UMBC/GES_486/486/project_2/Data/database/2008_2016py1.gpkg','2008_2016py1','ogr')

#year 1999_2007
G1999 = QgsVectorLayer('F:/UMBC/GES_486/486/project_2/Data/database/1999_2007.sqlite','1999_2007','ogr')
QgsProject.instance().addMapLayer(G1999)
G1999.selectByExpression("sizeclass = 'G'")
QgsVectorFileWriter.writeAsVectorFormat(G1999, r'F:/UMBC/GES_486/486/project_2/Data/database/1999_2007py.gpkg', 'utf-8', G1999.crs(),'GPKG', True)
iface.addVectorLayer('F:/UMBC/GES_486/486/project_2/Data/database/1999_2007py.gpkg','1999_2007py','ogr')

#year 1990_1998
G1990 = QgsVectorLayer('F:/UMBC/GES_486/486/project_2/Data/database/1990_1998.sqlite','1990_1998','ogr')
QgsProject.instance().addMapLayer(G1990)
G1990.selectByExpression("sizeclass = 'G'")
QgsVectorFileWriter.writeAsVectorFormat(G1990, r'F:/UMBC/GES_486/486/project_2/Data/database/1990_1998py.gpkg', 'utf-8', G1990.crs(),'GPKG', True)
iface.addVectorLayer('F:/UMBC/GES_486/486/project_2/Data/database/1990_1998py.gpkg','1990_1998py','ogr')

#year 1981_1989
G1981 = QgsVectorLayer('F:/UMBC/GES_486/486/project_2/Data/database/1981_1989.sqlite','1981_1989','ogr')
QgsProject.instance().addMapLayer(G1981)
G1981.selectByExpression("sizeclass = 'G'")
QgsVectorFileWriter.writeAsVectorFormat(G1981, r'F:/UMBC/GES_486/486/project_2/Data/database/1981_1989py.gpkg', 'utf-8', G1981.crs(),'GPKG', True)
iface.addVectorLayer('F:/UMBC/GES_486/486/project_2/Data/database/1981_1989py.gpkg','1981_1989py','ogr')


#setting active layer and symbology
active_layer = iface.activeLayer()

renderer = active_layer.renderer()

symbol = renderer.symbol()

# Setting color of active layer to red
symbol.setColor(QColor('red'))

#Refreshing symbology and legend
active_layer.triggerRepaint()

iface.layerTreeView().refreshLayerSymbology(active_layer.id())

#Opening attribute table
iface.showAttributeTable(iface.activeLayer())


```
## GIF
#### Slow
![](https://media.giphy.com/media/1oEtJUaxV563V52lhj/giphy.gif)

[Backup link](https://giphy.com/gifs/1oEtJUaxV563V52lhj/html5)
#### Fast
![](https://media.giphy.com/media/uFkgRxSI6XdLDUbsVF/giphy.gif)

[Backup link ](https://giphy.com/gifs/uFkgRxSI6XdLDUbsVF/html5)
