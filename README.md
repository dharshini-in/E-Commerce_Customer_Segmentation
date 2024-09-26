# E-Commerce_Customer_Segmentation
# E-Commerce_Customer_Segmentation

## Abstract:
* A key challenge for e-commerce businesses is to analyze the trend in the market to increase their sales. The trend can be easily observed if the companies can group the customers; based on their activity on the e-commerce site. This grouping can be done by applying different criteria like previous orders, mostly searched brands and so on.

## Problem Statement:
* Given the e-commerce data, use a k-means clustering algorithm to cluster customers with similar interests.

## Dataset Information:
* The data was collected from a well-known e-commerce website over a period of time based on the customer’s search profile.

## Scope:
* Analyzing the existing customer data and getting valuable insights about the purchase pattern
* Data pre-processing including missing value treatment
* Segmenting customers based on the optimum number of clusters (‘k’) with the help of silhouette score

#  What is K - Means clustering algorithm?

* K-Means clustering is a popular unsupervised machine learning algorithm used for partitioning a given dataset into K distinct clusters. The goal of the algorithm is to group similar data points together and separate dissimilar ones based on their feature similarity. The "K" in K-Means represents the predefined number of clusters that the algorithm aims to create.

* The K-Means clustering algorithm works as follows:

    1. Initialization: Randomly select K initial cluster centroids, which act as the centre points of the clusters.

    2. Assignment: Assign each data point to the cluster whose centroid is closest to it. This is typically done by measuring the Euclidean distance or another distance metric between the data point and each centroid.

    3. Update: Recalculate the cluster centroids by taking the mean of all the data points assigned to each cluster. This step adjusts the centroid positions.

    4. Iteration: Repeat steps 2 and 3 until convergence is reached. Convergence occurs when the assignment of data points to clusters and the positions of the centroids no longer change significantly.

    5. Output: The algorithm provides the final cluster assignments, where each data point belongs to a specific cluster.

* The objective of K-Means clustering is to minimize the sum of squared distances between the data points and their respective cluster centroids. By iteratively adjusting the centroids, the algorithm attempts to find the optimal cluster configuration that minimizes the within-cluster variation.

* It is important to note that K-Means clustering requires the number of clusters (K) to be specified beforehand, which can be a challenge if the optimal number of clusters is unknown. The algorithm is also sensitive to the initial placement of cluster centroids, and different initializations can lead to different clustering results.

* K-Means clustering has a wide range of applications in various domains, including customer segmentation, image segmentation, text mining, and anomaly detection. Its simplicity, efficiency, and scalability make it a popular choice for exploratory data analysis and pattern recognition tasks. However, it is essential to evaluate the results and consider alternative clustering algorithms if the data does not adhere well to the assumptions of K-Means, such as clusters of different sizes or non-linearly separable data.

# What is silhouette score?

The silhouette score is a metric used to evaluate the quality of clustering results. It measures how well each data point fits into its assigned cluster based on both the proximity to data points in its own cluster and the proximity to data points in neighbouring clusters.

The silhouette score ranges from -1 to 1, where:
- A score close to +1 indicates that the data point is well-clustered and is significantly closer to the data points in its own cluster compared to neighboring clusters.
- A score close to 0 indicates that the data point is close to the decision boundary between two clusters.
- A score close to -1 indicates that the data point may have been assigned to the wrong cluster and would be better off in a different cluster.

The silhouette score is calculated as follows for each data point:

1. Calculate the average distance between the data point and all other data points within the same cluster. This value is denoted as "a".

2. For each neighbouring cluster (clusters other than the assigned cluster), calculate the average distance between the data point and all the data points in that neighbouring cluster. Take the minimum of these values, denoted as "b".

3. Compute the silhouette score for the data point using the formula:
   **silhouette_score = (b - a) / max(a, b)**

4. Repeat steps 1 to 3 for all data points in the dataset.

The overall silhouette score is the average silhouette score across all data points in the dataset. A higher average silhouette score indicates better-defined and well-separated clusters.

The silhouette score is commonly used to evaluate the quality of clustering algorithms, assess the optimal number of clusters, or compare different clustering results. It provides a quantitative measure of how well the data points are clustered and can help in choosing the most appropriate clustering solution for a given dataset.

# Moto of project

* Find the most buying brands or most search brands based on given data by using K - Means clustering algorithm.

# Steps 

* Import required library
* Upload data 
* Data preprocessing
* Exploratory Data Analysis (EDA)
* K - Mean cluster
    1) Scaling
    2) Finding the optimum number of clusters (‘k’) with the help of the silhouette score
    3) Create a K-means Model
    4) Analysis of the result based on clusters and prediction of the final result
