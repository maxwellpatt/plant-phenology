# Plant Phenology Assessment in Santa Clara River Vicinity

## Summary
This repository contains a project focused on evaluating plant phenology near the Santa Clara River, which spans from Santa Clarita to Ventura. Phenology, or the study of life cycle events, plays a crucial role in understanding ecological synchronization and its disruptions due to climate change. This project utilizes a time series of Landsat imagery to assess phenological patterns across diverse plant communities, with implications for broader ecological dynamics.

## Objectives
The project aims to analyze the phenological behaviors of distinct plant communities along the Santa Clara River by examining:
- Riparian forests characterized by winter deciduous species like cottonwood and willow trees
- Grasslands, primarily comprising drought deciduous grasses
- Chaparral shrublands, dominated by evergreen shrubs
  
## Data Overview
The analysis leverages the Landsat OLI sensor's capabilities, utilizing eight pre-processed scenes:
- Level 2 surface reflectance products with erroneous values set to NA
- Scaled reflectance values to 100 for consistency
- Spectral bands 2-7 used for detailed vegetation assessment
- Scene dates encoded in filenames for temporal tracking
- Study sites are mapped as polygons, each annotated with the plant community type to facilitate targeted analysis

## Approach
The methodology involves:
- Transforming spectral reflectance into NDVI, a proxy for vegetation productivity
- Tracking NDVI variations over the year to capture phenological shifts
- Summarizing and comparing NDVI metrics within plant communities
- Visualizing NDVI trajectories to infer ecological responses to climate dynamics

## Workflow
The R programming environment is the backbone of our workflow, augmented by a suite of libraries to handle geospatial data, visualization, and statistical analysis. The process encompasses:
- Defining a function to calculate NDVI from spectral bands
- Applying this function to individual scenes and generating NDVI layers
- Streamlining the NDVI computation across all scenes using a custom function
- Extracting NDVI values at specific study sites representing various vegetation communities
- Cleaning and structuring the resultant data for clarity and ease of analysis
- Creating visualizations that show seasonal vegetation productivity patterns across different ecosystems
