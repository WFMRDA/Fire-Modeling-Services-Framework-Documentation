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

+------------------+---------+----------+-----------------------+-------------------------------------------------------------+
| Param            | type    | Required | Options               | Description                                                 |
+==================+=========+==========+=======================+=============================================================+
|"West Longitude"  | number  | *true*   |-180 and +180          | *Decimal Degrees only*                                      |
|                  |         |          |                       | Cannot be more than "East Longitude"                        |
+------------------+---------+----------+-----------------------+-------------------------------------------------------------+
|"East Longitude"  | number  | *true*   |-180 and +180          | *Decimal Degrees only*                                      |
|                  |         |          |                       | Cannot be less than "West Longitude"                        |
+------------------+---------+----------+-----------------------+-------------------------------------------------------------+
|"North Latitude"  | number  | *true*   |-90 and +90            | *Decimal Degrees only*                                      |
|                  |         |          |                       | Cannot be less than "South Latitude"                        |
+------------------+---------+----------+-----------------------+-------------------------------------------------------------+
|"South Latitude"  | number  | *true*   |-90 and +90            | *Decimal Degrees only*                                      |
|                  |         |          |                       | Cannot be more than "North Latitude"                        |
+------------------+---------+----------+-----------------------+-------------------------------------------------------------+
|"Landfire Year"   | number  | *true*   | - 2012                +                                                             |
|                  |         |          | - 2014                +                                                             |
+------------------+---------+----------+-----------------------+-------------------------------------------------------------+
|"Resolution"      | integer | *true*   | 30 - 10000            |                                                             |
+------------------+---------+----------+-----------------------+-------------------------------------------------------------+
|"Fuel Model Type" | integer | *true*   | - 40                  |                                                             |
|                  |         |          | - 13                  |                                                             |
+------------------+---------+----------+-----------------------+-------------------------------------------------------------+
|"Edit Rules"      | string  | *true*   |  See `Edit Rules`_    |                                                             |
+------------------+---------+----------+-----------------------+-------------------------------------------------------------+
|"Generate Geotiff"| boolean | *true*   |                       |                                                             |
+------------------+---------+----------+-----------------------+-------------------------------------------------------------+

Response
--------



.. _`Edit Rules`:

Edit Rules
----------