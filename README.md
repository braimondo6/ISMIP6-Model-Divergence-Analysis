# Quantifying and Attributing Ice Sheet Model Divergence Across Greenland's Drainage Basins

This repository contains Python codes for analyzing ice thickness change data across Greenland's drainage basins using machine learning techniques. The primary goal is to identify patterns of model divergence, cluster these patterns, and attribute the drivers of these clusters using explainable AI methods, finally mapping the insights back to geographical space.

## Project Overview

Understanding the sources of divergence among ice sheet models is crucial for improving projections of sea-level rise. This project employs a data-driven approach to:

1.  **Reduce dimensionality** of complex ice thickness change data.

2.  **Cluster** regions or models exhibiting similar divergence patterns.

3.  **Interpret** the features (e.g., initial year, initial SMB) that primarily drive these identified clusters.

4.  **Visualize** the results spatially to provide geographical context.

## Methodology

The analysis pipeline involves several key steps:

### 1. Principal Component Analysis (PCA)

* **Purpose:** PCA is applied to the ice thickness change data to reduce its dimensionality while retaining the most significant variance. This helps in identifying the primary modes of variability or divergence within the dataset, making subsequent clustering more effective and computationally efficient.

* **Output:** The PCA transforms the original high-dimensional data into a lower-dimensional PCA space, where each principal component represents a specific pattern of ice thickness change.

### 2. K-Means Clustering

* **Purpose:** Following PCA, K-Means clustering is utilized to group the model data points based on their similarity in the reduced PCA space. This helps in identifying distinct categories or behaviors of ice sheet change or model responses.

* **Output:** The clustering assigns each model's data point to a specific cluster, revealing natural groupings within the data.

### 3. SHAP (SHapley Additive exPlanations) for Cluster Interpretation

* **Purpose:** To understand why data points are assigned to specific K-Means clusters, SHAP (SHapley Additive exPlanations) values are computed. SHAP is an explainable AI (XAI) method that quantifies the contribution of each input feature (e.g., different climate model forcings, physical parameters) to the prediction (in this case, cluster assignment).

* **Output:** SHAP analysis provides insights into which model features or environmental variables are most influential in defining the characteristics of each identified cluster.

### 4. Spatial Mapping and Visualization

* **Purpose:** The abstract results from PCA and K-Means clustering are mapped back to their physical geographical locations within Greenland's drainage basins. This allows for a direct visual interpretation of the identified patterns and clusters on a map.

* **Output:** Spatial maps illustrating the distribution of PCA components, cluster assignments, and potentially feature importance from SHAP analysis across Greenland.


## Contact

For any questions or further information, please contact Ben Raimondo at bcraimon@buffalo.edu
