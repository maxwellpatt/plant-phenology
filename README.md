# Plant Phenology Assessment in Santa Clara River Vicinity

## Summary
This repository contains a project focused on evaluating plant phenology near the Santa Clara River, which spans from Santa Clarita to Ventura. Phenology, or the study of life cycle events, plays a crucial role in understanding ecological synchronization and its disruptions due to climate change. This project utilizes a time series of Landsat imagery to assess phenological patterns across diverse plant communities, with implications for broader ecological dynamics.

## Objectives
The project aims to analyze the phenological behaviors of distinct plant communities along the Santa Clara River by examining:
- Riparian forests characterized by winter deciduous species like cottonwood and willow trees
- Grasslands, primarily comprising drought deciduous grasses
- Chaparral shrublands, dominated by evergreen shrubs

## Repository Structure
```
├── data 
│ ├── landsat-data 
│ └── study_sites
├── analysis.RMD
├── analysis.html
├── .RData
├── .Rhistory
├── README.md 
└── .gitignore
```


  
## Data 
The analysis leverages the Landsat OLI sensor's capabilities, utilizing eight pre-processed scenes:
- Level 2 surface reflectance products with erroneous values set to NA
- Scaled reflectance values to 100 for consistency
- Spectral bands 2-7 used for detailed vegetation assessment
- Scene dates encoded in filenames for temporal tracking
- Study sites are mapped as polygons, each annotated with the plant community type to facilitate targeted analysis
Data are stored in the .gitignore and can be downloaded through this link: https://drive.google.com/drive/folders/1ON8FbDqcTjg2PKHmNGgyN7odTqpOnXla

Landsat data: “Operational Land Imager.” NASA, December 9, 2021. https://landsat.gsfc.nasa.gov/satellites/landsat-8/spacecraft-instruments/operational-land-imager/. 

## Approach
The methodology involves:
- Transforming spectral reflectance into NDVI, a proxy for vegetation productivity
- Tracking NDVI variations over the year to capture phenological shifts
- Summarizing and comparing NDVI metrics within plant communities
- Visualizing NDVI trajectories to infer ecological responses to climate dynamics

## Workflow
R is the coding language used, along with libraries to handle geospatial data, visualization, and statistical analysis. The process encompasses:
- Defining a function to calculate NDVI from spectral bands
- Applying this function to individual scenes and generating NDVI layers
- Streamlining the NDVI computation across all scenes using a custom function
- Extracting NDVI values at specific study sites representing various vegetation types
- Cleaning and structuring the resultant data for clarity and ease of analysis
- Creating visualizations that show seasonal vegetation patterns across different ecosystems
