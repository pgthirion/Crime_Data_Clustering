# Crime Data Dimensionality Reduction & Clustering 🔍

This project implements unsupervised machine learning techniques to analyze crime data. It focuses on using **Principal Component Analysis (PCA)** to reduce dataset dimensionality, followed by **K-Means** and **Hierarchical Clustering** to identify distinct crime profiles across different regions.

## 📊 Project Overview
**Context:** Unsupervised Learning assignment for the Stellenbosch University / HyperionDev Data Science Bootcamp.
**Goal:** To explore the `UsArrests` dataset, standardize the data, reduce features using PCA, and group locations with similar crime statistics into actionable clusters.

## 🛠️ Technologies Used
* **Python 3** (Jupyter Notebook)
* **Scikit-Learn:**
    * `PCA`: For reducing 4D crime data (Murder, Assault, UrbanPop, Rape) into principal components.
    * `KMeans`: For partitioning observations into k clusters.
    * `AgglomerativeClustering`: For hierarchical merging of clusters.
    * `StandardScaler`: For normalizing data to zero mean and unit variance.
* **Seaborn & Matplotlib:** For correlation heatmaps and dendrogram visualizations.
* **Pandas:** For data manipulation and reading `summary.csv` / `countries.csv`.

## 🔎 Key Analysis Steps
1.  **Exploratory Data Analysis (EDA):**
    * Analyzed data distribution and generated correlation heatmaps to visualize relationships between crime types (e.g., Murder vs. Assault).
    * Utilized `summary.csv` for statistical overview.
2.  **Dimensionality Reduction (PCA):**
    * Standardized the dataset to prevent features with larger scales (like 'Assault') from dominating the variance.
    * Calculated and plotted Principal Components to determine the optimal number of dimensions to retain.
3.  **Clustering Implementation:**
    * **K-Means:** Applied the Elbow Method to find the optimal 'k' and segmented states into specific risk groups.
    * **Hierarchical:** Generated Dendrograms to visualize the nested grouping of states based on euclidean distance.

## 📈 Findings
* The analysis successfully grouped regions into clear safety categories (e.g., "High Risk," "Moderate," "Low Risk").
* PCA revealed that violent crimes are strongly correlated, forming a primary component of variance, while urbanization is a secondary factor.

## 🚀 How to Run
1. Ensure the data files (`UsArrests.csv`, `countries.csv`, `summary.csv`) are in the root of this directory.
2. Install the required libraries:
   ```bash
   pip install -r requirements.txt
