
**This part is to get the flood map and asses the flood hazard.**

Python: 

*The code "Thresholding" will allow the water extension of the image pre- and post-disaster using a thresholding approach. We use four thresholds: Ostu Standard deviation, Triangle, and Threshold_minimum.
*The code "Performance_thresholding" compares the pre- and post-disaster water mask based on Sentinel-1 with the NDWI (ground truth) collected with Sentinel-2 a few days later. We can get the best flood mask with the best intersection over Union (IoU) and Recall by comparing the four thresholds with the ground truth.
*The code "Change_detrection_SAR" subtracts the image pre and post-disaster with the best performance to get the flood areas only.


QGIS:

Once you have your flood map, you can use the tool "Georeferencer" to georeference it based on the satellite images and "Polygonize" to transform it into a polygon. 

