# Unsupervised-ML-Clustering

## Steps involved in this project
#### 1. Data Prepa.
   -  Read in the data file wholesale_clients.csv
   -  Remove the Channel (restaurant, hotel, etc.) and Region columns since they are not fields we want to model on
   -  Note the number of rows and columns
   -  Standardize the data
   -  Double check that all the column means are 0 and standard deviations are 1
#### 2. K-Means Clustering
   -  Import KMeans and write a loop to fit models with 2 to 15 clusters
   -  Create an inertia plot
   -  scatter plot of the inertia values vrs the number of clusters
   -  Identify the elbow of the plot and fit a KMeans model just for that number of clusters
   -  Find the number of clients in each cluster
   -  Create a heat map of the cluster centers
   -  Name the clusters
   -  create a silhouette scores plot instead of an inertia plot
   -  fit two models with the number of clusters for the two highest silhouette scores and name the clusters
#### 3. Hierarchical Clustering
   -  Create a dendrogram using the scaled data
   -  Visually identify the number of clusters and update the color threadshold from the dendrogram
   -  Fit an agglomerative clustering model on the scaled data set with the "best" clusters and view the number of data points in each cluster
   -  Create a cluster map of the model you just fit
   -  Within the clustermap function, add z_score=0 (scales data by row)
   -  write a loop to view the silhouette score for 2 to 20 clusters
   -  fit a model with the number of clusters for the highest silhouette score
#### 4. DBSCAN
   -  create tune_dbscan function
   -  Apply the dbscan function on the scaled data
   -  Sort the data by highest silhouette score
   -  Fit a DBSCAN model on the scaled data set with the best eps + min_samples values and view the number of data points in each cluster
#### 5. Compare Techniques
#### 6. Recommend Client Segments
   -  With the top model as the K-Means model with 3 clusters, review the results again
   -  view the cluster centers with heatmap
#### 7. Predict the Cluster of a New Client
   -  Given this new client, determine which cluster they fall into
   -  Scale the new client data using the same scaler object from the Data Prep step
   -  Make a prediction using the K-Means model with 3 clusters
