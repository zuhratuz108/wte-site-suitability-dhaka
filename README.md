# GIS-Based Waste-to-Energy Facility Suitability Assessment in Dhaka, Bangladesh

[![Research](https://img.shields.io/badge/Research-Waste--to--Energy-blue)](https://github.com/zuhratuz108)
[![GIS](https://img.shields.io/badge/Method-GIS--MCDA-green)](https://github.com/zuhratuz108)
[![Machine Learning](https://img.shields.io/badge/Method-Machine%20Learning-orange)](https://github.com/zuhratuz108)

## Overview

This research develops an integrated geospatial decision-support framework to identify suitable locations for Waste-to-Energy (WTE) facilities in Dhaka, Bangladesh.

The study combines Geographic Information Systems (GIS), the Analytical Hierarchy Process (AHP), machine learning, and Explainable Artificial Intelligence (XAI) to evaluate environmental risks, land-use constraints, infrastructure accessibility, demographic characteristics, and social considerations.

The primary aim is to support evidence-based planning of sustainable waste management infrastructure in a densely populated, flood-prone megacity.


## Methodological Framework

The research follows an integrated GIS–AHP–Machine Learning–XAI workflow.

### 1. Spatial Criteria Development

Eleven environmental, infrastructural, demographic, and social criteria were incorporated into the suitability assessment:

### 2. Geospatial Data Processing

The spatial datasets were processed using Google Earth Engine (GEE), QGIS, ArcGIS Pro, and Google Earth Pro.

Key datasets and sources include:
- Sentinel-1 SAR imagery for flood susceptibility assessment.
- Sentinel-2 imagery for supervised LULC classification.
- SRTM Digital Elevation Model for terrain information.
- OpenStreetMap for road networks and social facilities.
- WorldPop for population density.
- Existing landfill locations from field verification and secondary municipal sources.

Spatial layers were standardized at 30 m resolution using WGS 84 / UTM Zone 46N.

### 3. AHP-Based Suitability Assessment

The Analytical Hierarchy Process was applied to determine the relative importance of the selected criteria through pairwise comparisons.

The resulting weights were integrated through GIS-based weighted linear combination to generate the WTE suitability index.

The continuous suitability surface was classified into five categories:

- Very Low
- Low
- Moderate
- High
- Very High

### 4. Machine Learning Assessment

Four supervised regression models were evaluated:

- Decision Tree (DT)
- Random Forest (RF)
- Gradient Boosted Tree (GBT)
- Extreme Gradient Boosting (XGBoost)

The continuous GIS-AHP suitability score was used as the response variable, with the spatial criteria serving as predictors.

Model performance was evaluated using five-fold cross-validation and the following metrics:

- Coefficient of determination (R²)
- Mean Absolute Error (MAE)
- Root Mean Square Error (RMSE)

### 5. Explainable Artificial Intelligence

SHAP (SHapley Additive exPlanations) was used to interpret the selected machine learning model.

The analysis examined the relative contribution and direction of influence of individual spatial criteria, helping explain the factors behind the predicted suitability patterns.

### 6. Identification of Robust Candidate Zones

The GIS-AHP and machine learning suitability outputs were compared to identify areas classified as High or Very High by both approaches.

Contiguous suitable areas were grouped, and isolated patches smaller than 0.01 km² were excluded to identify more consistent candidate zones for further investigation.

## Key Findings

- Flood susceptibility emerged as the most influential criterion in WTE facility suitability assessment.
- Land use/land cover was the second most influential factor.
- Road accessibility and proximity to existing landfills also played important roles.
- XGBoost achieved the strongest model performance, with an R² of 0.905 ± 0.005.
- SHAP analysis highlighted flood susceptibility, landfill proximity, and land-use conditions as major contributors to model predictions.
- The integration of GIS-AHP and machine learning helped identify more consistent candidate zones for further assessment.

**Important:** The machine learning models reproduce the GIS-AHP-derived suitability pattern. They do not represent direct validation against the operational performance of existing WTE facilities.

## Software and Tools

- Google Earth Engine
- QGIS
- ArcGIS Pro
- Google Earth Pro
- Python
- Scikit-learn
- XGBoost
- SHAP




## Contact

For research collaboration or queries regarding this project, please contact the repository owner through GitHub.
