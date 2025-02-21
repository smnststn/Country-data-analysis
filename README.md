# Clustering of countries

This project uses machine learning to explore and visualize global development patterns by grouping countries based on their socioeconomic characteristics. The analysis uses a dataset of 192 countries, with various metrics like GDP, CO2 emissions, life expectancy, and internet use, etc. to identify clusters of countries with similar development profiles.

## Project Overview

### Data
The dataset, `CountryData.xlsx`, contains various socioeconomic indicators for 192 countries. 

The dataset has some missing values, which are handled through imputation using the mean value of each column. The data are scaled using `StandardScaler` before being used in the clustering algorithms to ensure all metrics contribute equally to the analysis.

### Objective
The main goal of this project is to group countries into clusters based on their similarities across a range of socioeconomic indicators. This helps in understanding global development patterns and allows for the identification of countries with similar development profiles.

### Models Used
- **K-Means Clustering**: This algorithm partitions countries into a predefined number of clusters, aiming to minimize within-cluster variance. The optimal number of clusters is determined using the Elbow Method and the Davies-Bouldin Index.
- **Agglomerative Hierarchical Clustering (AHC)**: This method builds a hierarchy of clusters, merging the closest ones iteratively.

### Visualizations
The project also includes several visualizations to aid in understanding the clustering results:
- **World Maps**: Showing the clusters geographically, allowing for a visual understanding of regional patterns.
- **Boxplots**: Comparing specific metrics across clusters, showing the distribution of values for each cluster.
- **Scatter Plots**: Showing the first two PCA components colored by cluster, allowing for a visual understanding of cluster separation in a reduced dimensional space.

## Key Steps

1.  **Data Loading and Preprocessing:**
    - Loading the data from the `CountryData.xlsx` file.
    - Handling missing values by imputing them with the mean of their respective columns.
    - Scaling the data using `StandardScaler`.
2.  **Model Building:**
    - Determining the optimal number of clusters for the K-Means model using the Elbow Method and the Davies-Bouldin index.
    - Applying the K-Means algorithm to create clusters of countries.
    - Applying the Agglomerative Hierarchical Clustering (AHC) algorithm to the data.
3.  **Cluster Mapping:**
    - Mapping AHC labels to KMeans labels for comparison and validation.
4.  **Visualizations:**
    - Displaying the clusters on a world map for geographical visualization.
    - Generating boxplots to compare specific metrics across different clusters.
    - Using PCA to reduce the dimensionality of the data to 2 components and creating scatter plots to visualize the clusters.
5.  **Principal Component Analysis (PCA)**:
    - Applying PCA to reduce the dimensionality of the data and identify key components.
    - Visualizing the clusters on the PCA scatter plot.

## Results
The project successfully grouped countries into clusters based on their socioeconomic indicators. The analysis suggests a three-cluster model that aligns well with the real-world classification of countries into developed, emerging, and developing categories. The first two principal components from PCA explain a significant portion of the data's variance, highlighting development and trade/globalization patterns.

## Implications
- The clustering analysis provides a clear view of the global development landscape.
- The analysis can be used to identify specific areas where countries need to improve (e.g., access to electricity, infant mortality).

## Libraries Used
- pandas
- numpy
- seaborn
- matplotlib
- scikit-learn
- geopandas
- kneed

## Setup
1. Ensure you have all the required libraries installed.
2. Upload the `CountryData.xlsx` file to the same directory as your Jupyter notebook.
3. Run the Jupyter notebook to reproduce the analysis and visualizations.
