# Crypto Clustering Challenge

## Overview

This project explores the impact of 24-hour and 7-day price changes on cryptocurrency clustering using unsupervised learning techniques. The objective is to determine whether cryptocurrencies can be grouped based on their price fluctuations. The analysis employs K-Means clustering and Principal Component Analysis (PCA) to optimize and visualize the results.

## Project Workflow

### 1. Data Preparation
- Imported and cleaned `crypto_market_data.csv`, then standardized features using `StandardScaler()`.
  
### 2. Clustering with K-Means
- Used the **Elbow Method** to determine the optimal number of clusters (k).
- Applied K-Means clustering to group cryptocurrencies based on their price changes.
- Visualized cluster assignments using scatter plots.

### 3. Dimensionality Reduction with PCA
- Reduced features to three principal components while retaining key variance.
- Reapplied K-Means clustering to PCA-reduced data.
- Compared clustering results between original and PCA-reduced data.

### 4. Results Comparison
- Compared elbow plots and cluster visualizations before and after PCA.
- Assessed whether PCA improved clustering performance.

## Analysis Findings

- **Optimal k Selection**: The Elbow Method identified an ideal number of clusters (4) for both the original and PCA-transformed datasets.
- **Clustering Results**:
  - K-Means effectively grouped cryptocurrencies based on price fluctuations.
  - PCA retained a high level of variance while reducing dimensionality, improving clustering efficiency.
- **Insights**:
  - Some clusters showed clear separation, indicating distinct price movement patterns.
  - PCA slightly improved performance, reducing noise without significant loss of information.

## Files

- **Crypto_Clustering.ipynb**: Jupyter Notebook containing the full analysis.
- **crypto_market_data.csv**: Raw dataset containing cryptocurrency market data.

## Setup and Dependencies

Ensure the following libraries are installed:

```python
import pandas as pd
import hvplot.pandas
import matplotlib.pyplot as plt
from sklearn.preprocessing import StandardScaler
from sklearn.decomposition import PCA
from sklearn.cluster import KMeans
```

## Running the Analysis
- Clone the repository and navigate to the project directory.
- Install dependencies as shown above.
- Run the Jupyter Notebooks to generate the analyses.