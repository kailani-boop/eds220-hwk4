# EDS 220 HW 4: Palisades and Eaton Fire Scars Through False Color

## About
This repo contains the fourth homework assignment for EDS 220, Working with Environmental Datasets. The course focuses on accessing, exploring, and analyzing real-world environmental data using Python.

This assignment uses Landsat 8 satellite imagery to visualize the burn scars from the January 2025 Palisades and Eaton fires in Los Angeles County. The notebook restores the geospatial information of a Landsat NetCDF file, creates true color and false color (SWIR, NIR, red) images, and maps the false color image with the Palisades and Eaton fire perimeters. False color imagery makes burned areas stand out because burned land reflects strongly in shortwave infrared and weakly in near-infrared, while healthy vegetation does the opposite.

## Repository Structure
```
eds220-hwk4
│   README.md                                # Overview of the repository
│   hwk4-task2-false-color-latimer.ipynb     # Jupyter notebook with analysis
│   .gitignore
```

## Data
The data is not stored in this repository.

- **Landsat 8 imagery** (`landsat8-2025-02-23-palisades-eaton.nc`): A clipped subset of Landsat 8 Collection 2 Level-2 surface reflectance data from February 23, 2025, containing the red, green, blue, near-infrared, and shortwave infrared bands. It was originally accessed through the Microsoft Planetary Computer, and is available through the [EDS 220 course Google Drive](https://drive.google.com/drive/folders/1USqhiMLyN8GE05B8WJmHabviJGnmAsLP?usp=sharing). It is intended for visualization and educational purposes only.
- **Fire perimeters** (`Eaton_Perimeter_20250121.geojson`, `Palisades_Perimieter_20250121.geojson`): Dissolved fire perimeters for the Eaton and Palisades fires as of January 21, 2025, from the [Palisades and Eaton Dissolved Fire Perimeters (2025)](https://egis-lacounty.hub.arcgis.com/datasets/ad51845ea5fb4eb483bc2a7c38b2370c) dataset on the LA County Enterprise GIS hub (source: CAL FIRE). Downloaded as GeoJSON.

To run the analysis, download the Landsat file and the fire perimeter data, place them in a `data/` folder at the root of this repository, and run the notebook from top to bottom.

## Author
Kailani Latimer ([GitHub](https://github.com/kailani-boop))

## References
- EDS 220 Assignment 4 instructions: [https://meds-eds-220.github.io/MEDS-eds-220-course/assignments/assignment4-palisades-eaton-fires.html](https://meds-eds-220.github.io/MEDS-eds-220-course/assignments/assignment4-palisades-eaton-fires.html)
- U.S. Geological Survey. (2020). *Landsat 8-9 Operational Land Imager / Thermal Infrared Sensor Level-2, Collection 2* [Dataset]. Accessed via Microsoft Planetary Computer. [https://planetarycomputer.microsoft.com/dataset/landsat-c2-l2](https://planetarycomputer.microsoft.com/dataset/landsat-c2-l2)
- Microsoft Open Source, McFarland, M., Emanuele, R., Morris, D., & Augspurger, T. (2022). *microsoft/PlanetaryComputer: October 2022* (2022.10.28). Zenodo. [https://doi.org/10.5281/zenodo.7261897](https://doi.org/10.5281/zenodo.7261897)
- Los Angeles County Enterprise GIS. (2025). *Palisades and Eaton dissolved fire perimeters (2025)* [Dataset]. Data source: CAL FIRE. Retrieved November 19, 2026, from https://egis-lacounty.hub.arcgis.com/datasets/ad51845ea5fb4eb483bc2a7c38b2370c
- Riebeek, H. (2014). *Why is that forest red and that cloud blue? How to interpret a false-color satellite image.* NASA Earth Observatory. [https://earthobservatory.nasa.gov/features/FalseColor](https://earthobservatory.nasa.gov/features/FalseColor)
- U.S. Geological Survey. *What are the band designations for the Landsat satellites?* [https://www.usgs.gov/faqs/what-are-band-designations-landsat-satellites](https://www.usgs.gov/faqs/what-are-band-designations-landsat-satellites)
- U.S. Geological Survey. *Common Landsat band combinations.* [https://www.usgs.gov/media/images/common-landsat-band-combinations](https://www.usgs.gov/media/images/common-landsat-band-combinations)
