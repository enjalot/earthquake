earthquake resilience
=====================

More earthquake simulation [data available](http://earthquake.usgs.gov/earthquakes/shakemap/global/shake/haywiredm7.05_se/#download)

[ESRI Shape files](https://github.com/enjalot/earthquake/tree/master/HazusSHP)  
[GeoJSON](https://github.com/enjalot/earthquake/tree/master/HazusGeoJSON)  
[TopoJSON](https://github.com/enjalot/earthquake/tree/master/HazusTopoJSON)  


## converting shp files to geojson
```
brew install gdal
for i in *.shp; do ogr2ogr -f geoJSON ../HazusGeoJSON/$i.json $i; done
```
[Reference](http://vallandingham.me/shapefile_to_geojson.html)


## converting shp files to topojson
```
for i in *.shp; do topojson -o ../HazusTopoJSON/$i.json $i; done
```
[topojson reference](https://github.com/mbostock/topojson/wiki/Command-Line-Reference)
[tutorial series with topojson + d3.js](http://blog.thematicmapping.org/2013/06/converting-shapefiles-to-topojson.html)
