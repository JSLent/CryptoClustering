# CryptoClustering
Repo for Module 19 Challenge

# Cryptocurrency Clustering Analysis
This project asked us to cluster cryptocurrencies using K-means clustering and Principal Component Analysis (PCA). The analysis includes data normalization, clustering with K-means, and dimensionality reduction with PCA to optimize and visualize the clusters.

## Installation
To run this notebook, you need to have the following libraries installed:

pandas
hvplot
scikit-learn
You can install these libraries using pip:
    pip install pandas hvplot scikit-learn

## Usage
Clone the repository.
Navigate to the project directory.
Open the Jupyter notebook and run the cells sequentially.

## Data Preparation
### Load the Data:
Load the cryptocurrency market data from a CSV file into a Pandas DataFrame.
Display sample data and generate summary statistics.

### Normalize the Data:
Use the StandardScaler module from scikit-learn to normalize the data.
Create a DataFrame with the scaled data and set the “coin_id” index from the original DataFrame as the index for the new DataFrame.

## Clustering Analysis
### Find the Best Value for k Using the Original Scaled Data:
Use the elbow method to find the best value for k.
Create a list with the number of k-values from 1 to 11.
Compute the inertia for each k and plot the elbow curve.
Determine the optimal value for k.

### Cluster Cryptocurrencies with K-means Using the Original Scaled Data:
Initialize the K-means model with the best value for k.
Fit the K-means model using the scaled data.
Predict the clusters and add a new column with the predicted clusters to the DataFrame.
Create a scatter plot to visualize the clusters.

## Principal Component Analysis (PCA)
### Optimize Clusters with PCA:
Perform PCA on the original scaled DataFrame to reduce the features to three principal components.
Retrieve the explained variance to determine how much information can be attributed to each principal component.
Create a new DataFrame with the PCA data and set the “coin_id” index from the original DataFrame as the index for the new DataFrame.

### Find the Best Value for k Using the PCA Data:
Use the elbow method on the PCA data to find the best value for k.
Create a list with the number of k-values from 1 to 11.
Compute the inertia for each k and plot the elbow curve.
Determine the optimal value for k.

### Cluster Cryptocurrencies with K-means Using the PCA Data:
Initialize the K-means model with the best value for k.
Fit the K-means model using the PCA data.
Predict the clusters and add a new column with the predicted clusters to the DataFrame.
Create a scatter plot to visualize the clusters.

## Results
Elbow Curves:
Compare the elbow curves for the original data and the PCA data to determine the optimal value for k.
Cluster Visualization:
Compare the scatter plots for the original data and the PCA data to visualize the clusters.

## Conclusion
Using fewer features to cluster the data, as achieved through PCA, results in more distinct and separated clusters. The PCA data shows clearer groupings compared to the original data, suggesting that reducing dimensionality can enhance the clarity and effectiveness of clustering.