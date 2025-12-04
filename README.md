# Visualizing fire scars through false color
### Homework 4 repository for UCSB's MEDS rpogram EDS 222 working with environmental datasets class.

# About
This repostiry contains a notebook `hwk4-task2-false-color.ipynb`, which analyzes data on the Eaton and Palisades Fires that occured in early Jaunary 2025. The fires devastated thousands of homes, displaced tens of thousands of residents, and caused severe ecological and infrastructural damage.
Using a combination of geospatial and tabular datasets, the notebook walks through the process of generating a map of the resulting fire scars.
A key component of this analysis is the creation of false-color imagery for the Eaton and Palisades Fires. By assigning infrared spectral bands to visible RGB channels, we highlight burn severity and the extent of fire damage. False-color imagery is a valuable tool for monitoring wildfire impacts and helps land managers and researchers assess ecosystem recovery and plan restoration strategies.

# Highlights
- Processing and exploring satellite imagery in NetCDF format
- Geospatial data exploration with GeoPandas and rasterio/xarray
- Vector-to-raster integration: clipping Landsat imagery using fire perimeter shapefiles
- Generating true-color and false-color composites from multi-band Landsat data
- Visualizing fire scars and Landsat reflectance data through custom geospatial plots

## Repository organization
```
├── eds220-hwk4
│   ├── LICENSE
│   ├── README.md
│   ├── data
│   │   ├── eaton_perimeter
│   │   │   ├── Eaton_Perimeter_20250121.cpg
│   │   │   ├── Eaton_Perimeter_20250121.dbf
│   │   │   ├── Eaton_Perimeter_20250121.geojson
│   │   │   ├── Eaton_Perimeter_20250121.prj
│   │   │   ├── Eaton_Perimeter_20250121.shp
│   │   │   └── Eaton_Perimeter_20250121.shx
│   │   ├── landsat8-2025-02-23-palisades-eaton.nc
│   │   └── palisades_perimeter
│   │       ├── Palisades_Perimeter_20250121.cpg
│   │       ├── Palisades_Perimeter_20250121.dbf
│   │       ├── Palisades_Perimeter_20250121.geojson
│   │       ├── Palisades_Perimeter_20250121.prj
│   │       ├── Palisades_Perimeter_20250121.shp
│   │       ├── Palisades_Perimeter_20250121.shx
│   │       └── Untitled.ipynb
│   └── hwk4-task2-false-color-Medrano.ipynb
```
# Data Access
**Landsat 8 Imagery:** 
The Landsat data (landsat8-2025-02-23-palisades-eaton.nc) is not included in this repository. The data was retrieved through the EDS 220 course shared Google Drive folder.
**Fire Perimeter Shapefiles:**
The fire perimeter data is not included in this repository. Access the shapefiles from ArcGIS Hub:
Palisades and Eaton Dissolved Fire Perimeters: [LA County REST web](https://egis-lacounty.hub.arcgis.com/maps/ad51845ea5fb4eb483bc2a7c38b2370c/about)
Download both shapefiles seperately and store them locally to reproduce the analysis.
**EJI Data** 

## The follow packages were used in this analysis
- `pandas` - Data manipulation and analysis
- `numpy` - Numerical operations
- `geopandas` - Vector geospatial data handling (shapefiles)
- `matplotlib` - Data visualization and plotting
- `xarray` - Multi-dimensional array handling and NetCDF file operations
- `rioxarray` - Geospatial raster data operations and CRS management




## References
Bennett, M. M., Chen, J. K., Alvarez León, L. F., & Gleason, C. J. (2022). The politics of pixels: A review and agenda for critical remote sensing. Progress in Human Geography, 46(3), 729–752. https://doi.org/10.1177/03091325221074691

Galaz García, C., Cawse-Nicholson, K., Frew, A., & Fontenot, R. (2024). EDS 220: Working with environmental datasets [Course materials]. Master of Environmental Data Science, Bren School of Environmental Science & Management, University of California, Santa Barbara. https://meds-eds-220.github.io/MEDS-eds-220-course/

NASA Earth Observatory. (n.d.). Why is that forest red and that cloud blue? How to interpret a false-color satellite image. https://earthobservatory.nasa.gov/features/FalseColor

Palisades and Eaton Dissolved Fire Perimeters. (2025). Fire perimeter shapefiles [Geospatial dataset]. ArcGIS Hub. https://hub.arcgis.com/maps/ad51845ea5fb4eb483bc2a7c38b2370c

U.S. Geological Survey. (2025). Landsat 8 Collection 2 Level-2 surface reflectance data [Satellite imagery dataset]. Microsoft Planetary Computer. https://planetarycomputer.microsoft.com/dataset/landsat-c2-l2

Centers for Disease Control and Prevention and Agency for Toxic Substances Disease Registry. [2024] Environmental Justice Index. Accessed [11/21/2025]. https://atsdr.cdc.gov/place-health/php/eji/eji-data-download.htm