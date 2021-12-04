# Hierarchial Clustering Algorithm

Mainly there are two types of Hierarchical Clustering:-

1. Agglomerative
2. Divisive&#x20;

### The Working Algorithm of Agglomerative Clustering

1. Each point in itself is treated as a cluster itself.
2. Compute the Distance Metric(L2 Distance).&#x20;
3. Merge the two closest clusters, update the distance metric.&#x20;
4. Repeat until there remains only one cluster.

### Cluster Representation&#x20;

The Cluster at each iteration can be visualized through a dendrogram. A dendrogram is a tree-based structure that helps you read two things the no. of clusters and the minimum distance between the cluster formation.&#x20;

![](<.gitbook/assets/image (15).png>)

### What was the need for it?&#x20;

We do not have to specify the number of clusters we want, in K-means the k was a hyperparameter which we needed to optimize, but in hierarchial clustering, with every iteration, the number of clusters changes hence can stop at any iteration to get a viable number of clusters according to your need.&#x20;

Another issue with the k-means clustering is that it assumes all directions are equally important for each cluster.&#x20;

![Clustering with k-Means](<.gitbook/assets/image (16).png>)

These groups are stretched towards the diagonal. As k-means only consider the distance to the nearest cluster center, it can't handle this kind of data.&#x20;

To solve this kind of problem we use DBSCAN(more about this later)

### Advantages&#x20;

1. No optimization for **K**.&#x20;
2. The dendrogram representation helps read the data better.&#x20;
3. can handle non-elliptic and non-convex data distribution.

### Disadvantages&#x20;

1. Can take more time than other clustering algorithms.&#x20;
2. Might be affected by outliers and noise (To handle use max-distance).



