---
title: Final Proposal
---

### Proposal
I am going to use the MDIMAP data on the Sea level change and the sea level wetland adaptations data in order to compare locations of Maryland where there will be the greatest impact on structures, environment or etc. This could be a buffer or spatial querying finding the areas of impact of the sea level increase and see which counties are effected the most.

### Question
How much impact will sea level cause in 2050 and 2100 and if any which counties are most affected. This could include but not limited to wetland increase, structure loss, housing, etc.

### Data
So far:

Maryland Political boundaries to break up Maryland by counties
http://data.imap.maryland.gov/datasets/maryland-political-boundaries-county-boundaries

Maryland Sea Level Rise Wetland Adaptation Areas
http://data.imap.maryland.gov/datasets/maryland-sea-level-rise-wetland-adaptation-areas

If the site works eventually!

Maryland Mean Sea Level By County in 2100

http://data.imap.maryland.gov/datasets/maryland-mean-sea-level-by-county-in-2100

Maryland Mean Sea Level By County in 2050
http://data.imap.maryland.gov/datasets/maryland-mean-sea-level-by-county-in-2050

Maybe Baltimore Property data could be assessed later. Data given to us by Professor Dillion.

### Tools
I want to do a hexagonal grid on the areas of impact from the sea level rise. Followed by a heat map with the most affected counties and or shorelines. I could create a DEM to make it look better and make the water symbology nice for resemblance. If I have time I will do a python query in order to do the impact calculations areas. Once again if I still have enough time I will use geoda to see what the Morans law does to the data and see any trends or correlations.

### Question answered
If the analysis goes smoothly I should have an output that highlights the areas where sea level rise either changes more land to wet land or causes so previous building parcels to be over taken.

### More Involved

This is going to be more involved due to the time restraint of this final project. I am going to try and incorporate as much as I learned into this project in order to show a cool project and practice my skills. I chose the following components above because even though we have done them in class this time restraint is the real reason why this project is harder.  
### Final Project 
[![progess](https://user-images.githubusercontent.com/42807889/50006788-e357a680-ff7c-11e8-8ea1-5e23d6d32713.jpg)](https://user-images.githubusercontent.com/42807889/50006788-e357a680-ff7c-11e8-8ea1-5e23d6d32713.jpg)
Progress working on the final project.

### Sea Level Rise Levels 0 ft
![sea_level_rise_0ftmap](https://user-images.githubusercontent.com/42807889/50250046-c4f31000-03ad-11e9-8486-96a004816e33.jpg)
### Sea Level Rise Levels 5 ft
![sea_level_rise_5ft_map](https://user-images.githubusercontent.com/42807889/50250043-c45a7980-03ad-11e9-83cb-a2471ed38d7f.jpg)
### Sea Level Rise Levels 10 ft
![sea_level_rise_10ft_map_test](https://user-images.githubusercontent.com/42807889/50250044-c45a7980-03ad-11e9-812a-8d11c07871cf.jpg)
### Sea Level Rise Levels 0 ft-10 ft
![sea_level_rise_0-10ft_map](https://user-images.githubusercontent.com/42807889/50249954-82313800-03ad-11e9-9dcf-4b88d07f5e0c.jpg)

### GIF of affected areas of Maryland
![](https://media.giphy.com/media/8qD5ayU6IGXWSKoVHo/giphy.gif)

### Hexagonal Analysis
![](https://media.giphy.com/media/7TnAfPk5nt0tKKW9om/giphy.gif)

A Hexagonal Grid was made in order to compare the effects of each increase in sea level rise. The hexagon grid has a scale of 1/32 ft for each hexagonal polygon. In order to compare the sea level rise I transformed the polygon SRL 5ft and SRL 10ft into a point shapefile. This allowed me to do a count point within polygon. This means that the points created from the sea level rise data resides in the form a point shape within the newly formed hexagonal grid. The tool count points within polygon result in a separate hexagonal grid but now weighted with the number of points from the sea level rise as seen above. the lighter the color on the magma scale the higher the number of sea level rise points were within the 1/32 hexagonal polygon. The results showed that more area by the SRL 10ft was more significant than the SLR 5ft by its point density.   

### Total Buildings affected with the rise of sea level
## Sea Level Rise 5 ft
![sea_level_rise5ft_building_ map](https://user-images.githubusercontent.com/42807889/50262576-03092780-03e0-11e9-9f30-f6c6ab600500.jpg)
## Sea Level Rise 10 ft 
![sea_level_rise10ft_building_map](https://user-images.githubusercontent.com/42807889/50262941-7eb7a400-03e1-11e9-9761-82b60e47d116.jpg)

This was created by using MDIMAP's Maryland Building Foot prints. The tool selection by location was to figure out the location, number of buildings, and total area of the affected 5 ft and 10 ft sea level rise. The tool runs by selecting the buildings with the polygon of SLR 5ft or SLR 10ft. This newly formed polygon shapefile was graduated symbolized into 8 classification according to the area size of the building. To figure out the amount of buildings affected by the sea level rise I opened the attribute table and recorded the number of records selected from the original foot prints shapefile. Finally, I obtained the information of how much total building area was affected by running the field calculator tool to create a new field on the selected features. Then used the expression tool on the newly formed Total Area field with the equation sum(ShapeSTAre) giving me the sum of all the areas recorded in the selected attribute table.

### Working GeoDA

## 5 ft Sea Level Rise Hexagonal Analysis
![5ft_count_clustermap](https://user-images.githubusercontent.com/42807889/50263086-27fe9a00-03e2-11e9-822a-e2637fab487d.JPG)

Morans I Cluster map of the distribution of counts of points within the hexagonla grid. The red shows that the points are High High meaning they are more clustered and similiar. 

![5ft_count_plot](https://user-images.githubusercontent.com/42807889/50263095-377de300-03e2-11e9-8ba3-9b6b0a3da672.JPG)

This scatter plot shows the magnitude of the clustering which is relatively mild and positive with a .612462 trend correlation. 

![5ft_count_significance](https://user-images.githubusercontent.com/42807889/50263116-482e5900-03e2-11e9-9423-9b0aee432e0e.JPG)

This is the significance map of the points within the hexagonal grid. 

![5ft_count_localg](https://user-images.githubusercontent.com/42807889/50263299-14076800-03e3-11e9-82bc-f86a18b79b3f.JPG)

This is the Local G distribution 5ft SLR points within hexagonal grid. Most of the clustering is in red while some of the colors are less significant. 

![5ft_count_localgsig](https://user-images.githubusercontent.com/42807889/50263298-14076800-03e3-11e9-9c5d-0f0c7decb3c5.JPG)

Signifcance cluster map of the Local G distribution. 

![5ft_univ_local_geary](https://user-images.githubusercontent.com/42807889/50263379-7496a500-03e3-11e9-9175-8715e7b3cf20.JPG)

The above map represents the Univariate Local Geary distribution. 

![5ft_univ_local_geary_sig](https://user-images.githubusercontent.com/42807889/50263378-7496a500-03e3-11e9-8534-bb1d0d146d0b.JPG)

The above map represents the Univariate Local Geary distribution significance map. 

##10 ft Sea Level Rise Hexagonal Analysis


![clustermap](https://user-images.githubusercontent.com/42807889/50263832-c5a79880-03e5-11e9-9595-d59c683bb655.JPG)

Morans Cluster map of the distribution of counts of points within the hexagonla grid. The red shows that the points are High High meaning they are more clustered and similiar. Morans I cluster map has a .611702  positive clustering realtionship.

![clustermap_plot](https://user-images.githubusercontent.com/42807889/50263833-c5a79880-03e5-11e9-9a83-b347b0849fea.JPG)

Plot representing the correlation between points. There is 

![clustermap_sig](https://user-images.githubusercontent.com/42807889/50263834-c6402f00-03e5-11e9-933d-02039e568956.JPG)

This is the significance map of the points within the hexagonal grid. 

![localg_cluster](https://user-images.githubusercontent.com/42807889/50263836-c6402f00-03e5-11e9-9527-140afd1e56d2.JPG)

Local G distribution of the points within grid, showing the correlation. 

![localg_clustersig](https://user-images.githubusercontent.com/42807889/50263837-c6402f00-03e5-11e9-8af4-b37d2f219d57.JPG)

Significance of each point in relation to the next. 

![univlocalgcluster](https://user-images.githubusercontent.com/42807889/50263838-c6402f00-03e5-11e9-821f-25c7f8b192d2.JPG)

Univariate Local Geary distribution of the data showing the correlation of points within grid. 

![univlocalgclustersig](https://user-images.githubusercontent.com/42807889/50263839-c6402f00-03e5-11e9-97dc-4bc8e2eaf185.JPG)

Univariate Local Geary significance map. 

![corre](https://user-images.githubusercontent.com/42807889/50263835-c6402f00-03e5-11e9-83fa-da7ccddfa8e6.JPG)

This represents the correlogram bar graph of the eclidean distance between points showing the relationship bewteen the point distances. The Blue color bar has the most frequency and falls between .5 and .9 positioned away from another point. 

![3dplot](https://user-images.githubusercontent.com/42807889/50263831-c5a79880-03e5-11e9-8a9f-f42fb4e899c2.JPG)

This is a visual representation of the distribution of number points clustering on a X,Y,Z 3D model. 




