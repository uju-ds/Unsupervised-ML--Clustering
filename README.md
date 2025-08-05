# Unsupervised-ML-Clustering

## Steps involved in this project
#### 1. Data Prepa.
   - a. Read in the data file wholesale_clients.csv
   - b. Remove the Channel (restaurant, hotel, etc.) and Region columns since they are not fields we want to model on
   - c. Note the number of rows and columns
   - d. Standardize the data
   - e. Double check that all the column means are 0 and standard deviations are 1
#### 2. K-Means Clustering
   - a. Import KMeans and write a loop to fit models with 2 to 15 clusters
   - b. Create an inertia plot
   - c. scatter plot of the inertia values vrs the number of clusters
   - d. Identify the elbow of the plot and fit a KMeans model just for that number of clusters
   - e. Find the number of clients in each cluster
   - f. Create a heat map of the cluster centers
   - g. Name the clusters
   - h. create a silhouette scores plot instead of an inertia plot
   - i. fit two models with the number of clusters for the two highest silhouette scores and name the clusters
#### 3. Hierarchical Clustering
   - a. Create a dendrogram using the scaled data
   - b. Visually identify the number of clusters and update the color threadshold from the dendrogram
   - c. Fit an agglomerative clustering model on the scaled data set with the "best" clusters and view the number of data points in each cluster
   - d. Create a cluster map of the model you just fit
   - e. Within the clustermap function, add z_score=0 (scales data by row)
   - f. write a loop to view the silhouette score for 2 to 20 clusters
   - g. fit a model with the number of clusters for the highest silhouette score
#### 4. DBSCAN
   - a. create tune_dbscan function
   - b. Apply the dbscan function on the scaled data
   - c. Sort the data by highest silhouette score
   - f. Fit a DBSCAN model on the scaled data set with the best eps + min_samples values and view the number of data points in each cluster
#### 5. Compare Techniques
#### 6. Recommend Client Segments
   - a. With the top model as the K-Means model with 3 clusters, review the results again
   - b. view the cluster centers with heatmap
#### 7. Predict the Cluster of a New Client
   - a. Given this new client, determine which cluster they fall into
   - b. Scale the new client data using the same scaler object from the Data Prep step
   - c. Make a prediction using the K-Means model with 3 clusters
