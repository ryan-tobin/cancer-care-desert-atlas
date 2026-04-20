# Cancer Care Desert Atlas: Philadelphia

## Overview
This project maps spatial access to premier cancer care facilities in Philadelphia. By combining US Census demographic data with OpenStreetMap network algorithms, this tool computes drive-time isochrones to identify healthcare "access deserts", which are vulnerable neighborhoods stratified by income that lack efficient transit access to advanced oncology care.

## Clinical Motivation
As a clinical professional transitioning into spatial data science, I built this tool to bridge the gap between oncogenomics and healthcare equity. While tumor biology dictates clinical treatment, spatial geography often dictates access. This project highlights who can realistically reach centers like CHOP, Penn Medicine, and Jefferson Health.

## Tech/Packages Used
* **Python**: Core data processing
* **GeoPandas & Shapely**: Spatial joins and polygon manipulation
* **OSMNX & NetworkX**: Street network retrieval and travel-time isochrone calculation
* **Folium**: Interactive web mapping
* **Census API**: Demographic data retrieval

## Methodology
1. **Demographic Mapping**: Pulled ACS 5-Year Estimates for Median Household Income via the Census API and joined them to Philadelphia TIGER/Line census tract shapefiles.
2. **Network Analysis**: Downloaded the drivable street network around six major Philadelphia hospitals using OSMNX.
3. **Isochrone Generation**: Calculated 15-minute and 30-minute drive-time travel bubbles using NetworkX ego graphs.
4. **Spatial Overlay**: Combined the socio-economic choropleth map with the drive-time polygons to visually isolate access gaps.

## View the Map
[Click here to view the live interactive web map](https://ryan-tobin.github.io/cancer-care-desert-atlas/)
