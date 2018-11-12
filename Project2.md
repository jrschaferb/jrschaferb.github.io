# Project 2  United states Wildfires

 Joshua SCHAFERBIEN   GES 486 11/11/18

## Data:

To begin with, my project used the United States Forest Service which contains the data from 1980-2016 Wildfires.

(https://wildfire.cr.usgs.gov/firehistory/data.html)

## Background
The united States Forest Service Provided us with information on the wildfires from 1980-2016. In the dataset there is 300,524 records of wildfires ranging from size class A to size class G.

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

With this in mind my project queried the years of 1981-2016 by sub dividing them into four 9 year periods:

#### 1981-1989
![1981_1989_class_g](https://user-images.githubusercontent.com/42807889/48329609-81bbb980-e617-11e8-8d57-a0b4aa9535e9.jpg)
#### 1990-1998
![1990_1998_class_g](https://user-images.githubusercontent.com/42807889/48330271-f55ec600-e619-11e8-88c0-6c42b61be677.jpg)
#### 1999-2007
![1999_2007_class_g](https://user-images.githubusercontent.com/42807889/48330284-04de0f00-e61a-11e8-88a8-104e13704514.jpg)
#### 2008-2016
![2008_2016_class_g](https://user-images.githubusercontent.com/42807889/48329710-dfe89c80-e617-11e8-938b-6e3ff4ec3dd0.jpg)
## Projections/coordinate system:

For this project I used the
CRS
EPSG:4326 - WGS 84 - Geographic projection since it is of the United States as a default.




## Tools used:
In QGIS v3.2 in order to create the GIF containing the time series Giphy was used to edit the photos. Just as a Back up for the data i placed all my shapefiles into a database. The selection by expression and selection by attribute were the most used tools in this lab.


## Python Code
```Python
from PyQt5.QtGu import QColor

from PyQt5.QtCore import Qt

from qgis.utils import iface

qgis.utils.iface.addRasterLayer("http://server.arcgisonline.com/arcgis/rest/services/ESRI_Imagery_World_2D/MapServer?f=json&pretty=true","raster")
qgis.utils.iface.addRasterLayer("http://server.arcgisonline.com/ArcGIS/rest/services/Canvas/World_Light_Gray_Base/MapServer?f=json&pretty=true","raster")
iface.addVectorLayer('F:/UMBC/GES_486/486/project_2/Data/wf_usfs_1980_2016/wf_usfs_1980_2016.shp','wf_usfs_1980_2016','ogr')

iface.addVectorLayer('F:/UMBC/GES_486/486/project_2/Data/database/1981_1989_class_G.sqlite','1981_1989_class_G','ogr')

iface.addVectorLayer('F:/UMBC/GES_486/486/project_2/Data/database/1990_1998_class_G.sqlite','1990_1998_class_G','ogr')

iface.addVectorLayer('F:/UMBC/GES_486/486/project_2/Data/database/1999_2007__class_G.sqlite','1999_2007__class_G','ogr')

iface.addVectorLayer('F:/UMBC/GES_486/486/project_2/Data/database/2008_2016_class_G.sqlite','2008_2016_class_G','ogr')

active_layer = iface.activeLayer()

renderer = active_layer.renderer()

symbol = renderer.symbol()

symbol.setColor(QColor('red'))

active_layer.triggerRepaint()

iface.layerTreeView().refreshLayerSymbology(active_layer.id())

iface.showAttributeTable(iface.activeLayer())

```
## GIF
![](https://media.giphy.com/media/1gRUSsjnCT7ICZexz0/giphy.gif)

![](https://media.giphy.com/media/XooXBsWAXHGRnZBrgn/giphy.gif)

[backup link 1](https://giphy.com/gifs/XooXBsWAXHGRnZBrgn/html5)

[backup link 2](https://giphy.com/gifs/1gRUSsjnCT7ICZexz0/html5)

