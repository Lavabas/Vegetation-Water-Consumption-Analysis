# Vegetation Water Consumption Analysis in an Agricultural Region of Sri Lanka Using MODIS NDVI and SSEBop Evapotranspiration Data
## Overview

This project investigates vegetation water consumption dynamics within a major agricultural region in Sri Lanka using remote sensing datasets and cloud-based geospatial analysis tools. The workflow integrates MODIS vegetation products with SSEBop evapotranspiration (ET) datasets through the Google Earth Engine (GEE) Python API and Xee/xarray framework.

The primary objective of this analysis is to estimate how much water is consumed by vegetated agricultural surfaces over time by combining vegetation extent and evapotranspiration rates. The workflow demonstrates how Earth Observation (EO) data can support agricultural water management, drought monitoring, and irrigation planning in data-scarce regions.

The selected study area represents an intensively cultivated agricultural landscape in Sri Lanka characterized by seasonal vegetation dynamics and irrigation-dependent farming activities.

## Study Area
The analysis was conducted over an agricultural region in Sri Lanka using a manually selected Region of Interest (ROI) in Google Earth Engine.

The region includes:
- Agricultural lands
- Irrigated cultivation areas
- Seasonal vegetation zones
- Mixed cropland landscapes

The ROI was selected to evaluate spatial and temporal changes in vegetation health and water consumption throughout the year 2023.

## Objectives

The main objectives of this study were:
1. Identify vegetated agricultural areas using NDVI thresholds
2. Estimate evapotranspiration patterns across the study area
3. Calculate temporal vegetation water consumption
4. Analyze seasonal variability in agricultural water use
5. Demonstrate integration of GEE + Xee + xarray workflows for EO analysis

<img width="685" height="624" alt="image" src="https://github.com/user-attachments/assets/02b2cf5d-13a9-42b0-9fe5-99de5cc0bd19" />

<img width="685" height="624" alt="image" src="https://github.com/user-attachments/assets/03cc2ac9-9291-43ad-b6ad-8f93377b393e" />

<img width="1338" height="3590" alt="image" src="https://github.com/user-attachments/assets/2a3830ce-ba49-4e3a-9ec3-586a9858c4b3" />

<img width="849" height="470" alt="image" src="https://github.com/user-attachments/assets/648fb1fe-e5f5-4ac7-b543-b3354b766945" />


## Datasets Used
1. MODIS NDVI Product
- Dataset: MODIS/061/MOD13Q1
- Parameters used: NDVI (Normalized Difference Vegetation Index)
- Spatial Resolution: 250 m
- Temporal Resolution: 16-day composites
- Purpose: Vegetation detection, Vegetation density estimation, Vegetation masking

2. SSEBop Evapotranspiration Product
- Dataset: OpenET/SSEBOP/CONUS/GRIDMET/MONTHLY/v2_0
- Parameter used: ET (Actual Evapotranspiration)
- Purpose:Estimation of vegetation water consumption and Surface water use analysis

## Tools and Libraries
1. Google Earth Engine (GEE)
2. Python API for GEE
3. Xee
4. xarray
5. geemap
6. matplotlib
7. NumPy

## Key Findings
1. The selected agricultural region exhibits extensive vegetation cover throughout the year.
2. Evapotranspiration patterns strongly vary seasonally.
3. Vegetation water consumption fluctuates significantly across months.
4. Remote sensing provides an effective method for estimating agricultural water use at regional scales.
5. GEE + Xee workflows enable efficient cloud-based EO analysis using Python.

## Limitations
1. Spatial Resolution Constraints

- MODIS products have moderate spatial resolution (250 m–500 m), which may not capture:
   - Small agricultural fields
   - Fine-scale irrigation patterns
   - Heterogeneous land cover structures

2. NDVI Threshold Sensitivity
- The vegetation mask depends on a fixed NDVI threshold: NDVI > 0.5
- Different thresholds may produce slightly different vegetation extents.

3. ET Product Limitations
- SSEBop ET products rely on modeled evapotranspiration estimates rather than direct field measurements.
- Uncertainties may arise from:
  1. Meteorological inputs
  2. Model assumptions
  3. Cloud contamination
  4. Surface heterogeneity

4. Temporal Aggregation
- MODIS and ET datasets use composited temporal intervals, which may smooth short-term variability.

5. Lack of Ground Validation
- The study did not include:
  - Field-based ET measurements
  - Soil moisture observations
  - Irrigation records
- Therefore, results should be interpreted as regional-scale EO-based estimates.

## Notes
1. Higher-resolution Sentinel-2 vegetation products can improve vegetation mapping.
2. Integration with rainfall and soil moisture datasets can further improve agricultural water-use assessments.
3. The methodology is suitable for drought monitoring and irrigation planning applications.
