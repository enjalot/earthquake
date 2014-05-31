earthquake resilience
=====================

### [d3 getting started notes](https://docs.google.com/document/d/1c06-5NIaaAurbwfxtnoQRCuFvKJdz1gcMCmlvfISUDc/edit?usp=sharing)

More earthquake simulation [data available](http://earthquake.usgs.gov/earthquakes/shakemap/global/shake/haywiredm7.05_se/#download)

Relevant [ESRI Shape files](https://github.com/enjalot/earthquake/tree/master/HazusSHP)  
Converted to [GeoJSON](https://github.com/enjalot/earthquake/tree/master/HazusGeoJSON)  
Converted to [TopoJSON](https://github.com/enjalot/earthquake/tree/master/HazusTopoJSON)  


## converting shp files to geojson
The following command was used on a Mac to generate the GeoJSON.
```
brew install gdal
for i in *.shp; do ogr2ogr -f geoJSON ../HazusGeoJSON/$i.json $i; done
```
[Reference](http://vallandingham.me/shapefile_to_geojson.html)


## converting shp files to topojson
The following command was used on a Mac to generate the TopoJSON.
```
for i in *.shp; do topojson -o ../HazusTopoJSON/$i.json $i; done
```

there are more options available in topojson, so you might want to convert yourself with a custom command.  
[topojson reference](https://github.com/mbostock/topojson/wiki/Command-Line-Reference)  
[tutorial series with topojson + d3.js](http://blog.thematicmapping.org/2013/06/converting-shapefiles-to-topojson.html)
