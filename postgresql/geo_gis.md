Geo-GIS
=======

While working with calculating distances with Postgresql and PostGis, I learned this:

* You can store latitude/longtitude in the type build-in type `point`
* A point can be constructed like this: `point(lat,lon)`
* Calculating distances between points in _meters_ with formula's you find on the internet are off > 10%
* Better use the PostGis extention:
  - Install extention: `CREATE EXTENSION postgis SCHEMA postgis;` 
  - Add the schema to the `search_path` variable (`SET search_path = "$user", public, postgis;`)
  - A point can be constructed like this: `ST_POINT(lon,lat)::geography`
  - Notice 1: lat/lon are swapped, lon goes first (because longitude can be seen as the x-axis)
  - Notice 2: you need to cast to geography, because default it's geometry
  - When using geography, `ST_DISTANCE(point1, point2)` returns meters
