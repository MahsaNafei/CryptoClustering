# Crypto Market Data Analysis

### Overview

This repository contains Python code for analyzing cryptocurrency market data using K-Means clustering and Principal Component Analysis (PCA). The analysis aims to identify clusters and patterns within the cryptocurrency market.

#### 1. Data Loading and Exploration

- Import necessary libraries and dependencies, including pandas, hvplot, scikit-learn's KMeans, PCA, and StandardScaler.
- Load cryptocurrency market data from the CSV file into a Pandas DataFrame.
- Display sample data, generate summary statistics, and plot the data to gain insights.

#### 2. Data Preparation

- Normalize the data using the `StandardScaler` module from scikit-learn to ensure uniform scaling.
- Create a DataFrame with the scaled data.
- Set the 'coin_id' column as the index.

#### 3. Find the Best Value for K Using the Original Data

- Use K-Means clustering on the original data to find the optimal number of clusters (K).
- Create an Elbow Curve by iterating through different values of K and computing the inertia for each.
- Identify the optimal K where the inertia reduction becomes less significant.

#### 4. Cluster Cryptocurrencies with K-Means Using the Original Data

- Initialize the K-Means model with the best value for K.
- Fit the model using the scaled data.
- Predict the clusters and add a new column to the DataFrame with the predicted clusters.
- Visualize the clusters using a scatter plot.

#### 5. Optimize Clusters with Principal Component Analysis (PCA)

- Create a PCA model with three principal components.
- Use PCA to reduce the dimensionality of the scaled data.
- Examine the explained variance of the three principal components.
- Analyze the total explained variance.

#### 6. Find the Best Value for K Using the PCA Data

- Use K-Means clustering on the PCA-transformed data to find the optimal number of clusters.
- Create an Elbow Curve for PCA to identify the optimal K.

#### 7. Cluster Cryptocurrencies with K-Means Using the PCA Data

- Initialize the K-Means model using the best value for K from PCA.
- Fit the model using the PCA-transformed data.
- Predict the clusters and visualize the results.

#### 8. Visualize and Compare the Results

- Contrast the Elbow curves for both the original data and PCA-transformed data.
- Compare the clusters obtained with and without PCA to analyze the impact of dimensionality reduction.

### Results and Conclusion

The analysis shows that using fewer features (principal components) in K-Means clustering, obtained through PCA, results in similar performance compared to the original model. The optimal number of clusters remains consistent at K=4. The use of PCA demonstrates reduced inertia and improved visualization of distinct clusters.

The trade-off between computational efficiency and information retention is highlighted, emphasizing the choice of features based on specific analysis goals. The visualizations provide insights into the clustering patterns and help interpret the impact of dimensionality reduction on the clustering results.


### Data Sources

The cryptocurrency market data used in this analysis is sourced from [Resouces](https://github.com/MahsaNafei/CryptoClustering/blob/main/Resources/crypto_market_data.csv). Ensure that you comply with the terms of use and licensing agreements associated with the data source.

### Instructions

1. Install Dependencies:
   - Ensure you have Python installed on your machine.
   - Install the required Python libraries 

2. Run the Jupyter Notebook:
   - Open the "crypto_market_analysis.ipynb" notebook.

3. Execute the Code:
   - Run each cell in the notebook sequentially to execute the analysis step by step.

4. Review Results:
   - Review the visualizations and analysis results in the notebook to gain insights into cryptocurrency market clusters and patterns.


![3D PCA image](https://github.com/MahsaNafei/CryptoClustering/blob/main/Images/plot.png)

