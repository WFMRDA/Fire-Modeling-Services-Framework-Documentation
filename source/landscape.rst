Landscape Service
=================

The Landscape Service allows users to create, edit and download landscapes files.
Landscape files can be created in either geotiff or LCP which is a raster file comprised of spatial information representing topography (slope, elevation, and aspect), fuel model, and canopy characteristics including canopy cover, canopy base height, canopy height, and canopy bulk density.


Creating A Landscape
********************


Creating a landscape required a POST

Request Body
------------

.. note::
    Currently we only accept code :code:`x-www-form-urlencoded` payloads

+------------------+---------+----------+---------------------+
| Param            | type    | Required | Description         |
+==================+=========+==========+=====================+
|"West longitude"  | number  | *true*   |                     |
+------------------+---------+----------+---------------------+
|"East Longitude"  | number  | *true*   |                     |
+------------------+---------+----------+---------------------+
|"North Latitude"  | number  | *true*   |                     |
+------------------+---------+----------+---------------------+
|"South Latitude"  | number  | *true*   |                     |
+------------------+---------+----------+---------------------+
|"Landfire Year"   | number  | *true*   |                     |
+------------------+---------+----------+---------------------+
|"Resolution"      | integer | *true*   |                     |
+------------------+---------+----------+---------------------+
|"Fuel Model Type" | integer | *true*   |                     |
+------------------+---------+----------+---------------------+
|"Edit Rules"      | string  | *true*   |                     |
+------------------+---------+----------+---------------------+
|"Generate Geotiff"| boolean | *true*   |                     |
+------------------+---------+----------+---------------------+

Response


 