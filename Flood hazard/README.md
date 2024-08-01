
**This part is to get the flood map and asses the flood hazard.**

**Python:**

The code *"Thresholding"* will allow the water extension of the image pre- and post-disaster using a thresholding approach. We use four thresholds: Ostu Standard deviation, Triangle, and Threshold_minimum.

The code *"Performance_thresholding"* compares the pre- and post-disaster water mask based on Sentinel-1 with the NDWI (ground truth) collected with Sentinel-2 a few days later. By comparing the four thresholds with the ground truth, we can get the best flood mask with the best intersection over Union (IoU) and Recall.

The code *"Change_detrection_SAR"* subtracts the image pre and post-disaster with the best performance to get the flood areas only.



**QGIS:**

Once you have your flood map, you can use the tool *"Georeferencer"* to georeference it based on the satellite images and *"Polygonize"* to transform it into a polygon. 

To assess the flood hazard for each municipality, you can get the administrative boundary of each municipality in OpenStreetMap and then overlay the flood pixel map.

**First step:**


You can first calculate the total surface of the municipality in ha with the following instructions.

Click on the attribute table's *Field Calculator* icon (calculator symbol).

Check the box to create a new field.

Enter a name for your new field (e.g., Area_Ha).
.
Set the Output field type to Decimal number (double).

In the Expression box, enter the formula to calculate the area in hectares. To convert it, you can use the expression **$area / 10000**, which divides the area in square meters by 10,000. 

**Second step:**

Once you have the administrative boundaries for each municipality and the surface, you can overlay the flood pixel map with each administrative boundary with the tool *intersection*. Then, you can calculate the surface proportion of floods in each municipality.

