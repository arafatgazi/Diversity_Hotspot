# Ecological Diversity & Anomaly Detection System

An advanced ecological data analysis and anomaly detection framework built with Python. This project evaluates biodiversity health, patterns, and ecological disturbances across 56 distinct ecological compartments using multivariate statistics and unsupervised machine learning.

## 📌 Project Overview
Monitoring biodiversity and ecosystem health is critical for conservation. This project leverages ecological indices—such as **Taxa-Richness**, **Simpson's Diversity Index (1-D)**, **Shannon-Wiener Index (H)**, and **Pielou's Evenness (\(e^H/S\))**—to identify structural patterns and flag environmental anomalies. 

The pipeline automates data quality checking, scales metrics, reduces mathematical dimensions, clusters similar habitats, and statistically isolate ecological outliers (Degraded vs. Hotspot areas).

## 🚀 Key Features & Methodologies

1. **Exploratory Data Analysis (EDA):**
   * Computes **Spearman Rank Correlation** to map the non-linear relationships between diverse ecological indices.
   * Generates comprehensive pairplots for structural visual diagnostics.

2. **Dimensionality Reduction & Clustering:**
   * Utilizes **StandardScaler** to normalize varied physical scales across ecological indices.
   * Implements **Principal Component Analysis (PCA)** to condense multivariate data into 2 distinct spatial coordinates.
   * Applies **K-Means Clustering** to partition data points into distinct ecological similarity zones.

3. **Ecological Anomaly Detection:**
   * Calculates **Mahalanobis Distance** to identify multivariate outliers while accounting for correlations between structural indices.
   * Uses a **Chi-Square distribution test (df=4)** to assign precise p-values to sample points.
   * Categorizes habitat compartments into three distinct operational states based on a 95% confidence threshold:
     * 🟢 **Normal:** Balanced and typical biodiversity profiles.
     * 🔴 **Degraded / Outlier:** Statistically significant low diversity zones indicating critical ecological stress.
     * 🔵 **Hotspot / Outlier:** Exceptionally high diversity regions of supreme conservation priority.

## 🛠️ Tech Stack & Libraries
* **Language:** Python
* **Data Processing:** Pandas, NumPy
* **Statistical Analysis:** SciPy (Stats)
* **Machine Learning:** Scikit-Learn (PCA, KMeans, StandardScaler)
* **Data Visualization:** Seaborn, Matplotlib

## 📊 Core Visualizations Generated
* `Spearman_Corelation.png`: Visual distribution matrix mapping correlations among all target features.
* `Ecological_Anomaly_Plot.png`: Interactive scatter plot highlighting structural anomalies across all 56 compartments relative to the 95% confidence threshold.

## 📂 Project Structure
```text
├── DIVERSITY1.csv                  # Input ecological dataset
├── analysis_pipeline.py            # Primary Python analysis script
├── Spearman_Corelation.png         # Correlation pairplot output
├── Ecological_Anomaly_Plot.png    # Anomaly classification output
└── Ecological_Anomaly_Results.csv  # Final output dataset with computed metrics
```

## 📈 Intended Use Case
This system serves as an automated toolkit for ecologists, environmental scientists, and conservation agencies to dynamically ingest field-sampled taxonomic data, screen for local ecosystem degradation, and flag major bio-hotspots for immediate resource allocation.
