# K-means

Implementation of k-means clustering algorithm on Spark. We also try to understand  the impact of using various distance metrics and initialization strategies.

Let us say we have a set X of n data points in the d-dimensional space R^d. Given the number of clusters k and the set of k centroids C, we now proceed to define various distance metrics and the corresponding cost functions that they minimize.

We find the Euclidean distance, Euclidean cost, Manhattan distance and Manhattan cost.

Iterative k-Means Algorithm: k centroids are initialized, each point is assigned to the nearest centroid and the centroids are recomputed based on the assignments of points to clusters. In practice, the above steps are run for several iterations. 

Dataset: 
* data.txt contains the dataset which has 4601 rows and 58 columns. Each row is a document represented as a 58-dimensional vector of features. Each component in the vector represents the importance of a word in the document. 
* c1.txt contains k initial cluster centroids. These centroids were chosen by selecting k = 10 random points from the input data.
* c2.txt contains initial cluster centroids which are as far apart as possible. (You can do this by choosing 1st centroid c1 randomly, and then finding the point c2 that is farthest from c1, then selecting c3 which is farthest from c1 and c2, and so on).

I have also explored the initialization strategies with Euclidean distance and with Manhattan distance and compared the results. I have also talked about whether random initialization of k-means using c1.txt better than initialization using c2.txt in terms of cost φ(i)
