We obtained the flood map of the  region then we can start on QGIS the Buildings an population exposure.

**Buildings exposure**

You can download the Microsoft Building Footprints data at this link: https://github.com/microsoft/GlobalMLBuildingFootprints.

WE overlay each city's administrative boundary with the footprint to get the number of buildings in the municipality. Secondly, you can overlay the flood map obtained for each municipality or the global flood map with the buildings with the QGIS tool *intersection*. Then, in the "attribute table," you can see the number of flooded buildings.


**Population exposure**

You can download the population at this link: https://www.worldpop.org/. We can follow the method for the building exposure. We can calculate the total number of people in each municipality and the number of people flooded with the tool * Zonal statistic*.
