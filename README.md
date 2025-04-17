# GIS files of electoral districts

This repository contains GIS files used by Poliwave.
Each district folder contains README.md and LICENSE files from their government or electoral office.
Poliwave does not own these files, and they are provided for convenience.

## File Format

The GIS files are in the shapefile format, which is a popular geospatial vector data format for geographic information system (GIS) software. Each shapefile consists of several files with the same base name but different extensions. The main file has the `.shp` extension, while other associated files include `.shx`, `.dbf`, and others.

This repository also contains GeoJSON files, which are a format for encoding a variety of geographic data structures. GeoJSON is based on JavaScript Object Notation (JSON) and is widely used for web mapping applications.

When GeoJSON files are available from the electoral office website, they are preferred over shapefiles for their simplicity and ease of use in web applications. Otherwise, the GeoJSON files are generated from the shapefiles using the `ogr2ogr` command-line tool from the GDAL library.

To convert shapefiles to GeoJSON, the following command is used:

```bash
ogr2ogr -f "GeoJSON" output.geojson input.shp
```

This command converts the shapefile `input.shp` to a GeoJSON file named `output.geojson`. The resulting GeoJSON file can be used in web applications and other GIS software that supports the GeoJSON format.

Shapefiles can also be converted to GeoJSON using [QGIS](https://qgis.org). Follow these [instuctions](https://gist.github.com/YKCzoli/b7f5ff0e0f641faba0f47fa5d16c4d8d) to convert shapefiles to GeoJSON using QGIS.
