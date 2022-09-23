# Network-Analysis

## Hierarchical and Spectral Clustering

In this project we consider the dolphin data set. Each row in the dataset corresponds to one of the N=62 bottlenose dolphins in the studied network. We have three sources of information:

1. A set of features characterising each individual. This information is given as a N x p feature matrix F,
where N=62 samples with p=32 features capturing different traits of the dolphins.

2. The social network of associations between the individual dolphins. The N=62 nodes of the graph are
the individuals and the E=159 edges correspond to the frequent associations between them. This
information is given as a N x N adjacency matrix, A.

3. A table listing the dolphin names ordered according to the rows of the feature and adjacency matrices.
You may use these names in analysing or presenting some of your findings.

First we employ hierarchical clustering to cluster the feature matrix F. We use average linkage and take Euclidean distance as the distance.

Then we code a function to calculate the Silhouette Score of a given clustering and using that function we compute the Silhouette Score for all the clusterings obtained at all the levels of hierarchical clustering, from finest to coarsest. Then we determine what level is optimal.

## Graph-based Analysis

In this subtask, we will analyse the dolphin social network, i.e. the graph of frequent associations encoded
by the adjacency matrix A.

### Spectral clustering

Using only NumPy/SciPy, we compute the normalized Laplacian of the dolphin network, and its two smallest eigenvalues (and corresponding eigenvectors). We comment on these values and use them to obtain a spectral partition of the graph into two sets of nodes.

### Centralities Analysis

We consider three measures of centrality: PageRank, degree centrality, and eigenvector centrality. We apply them to the dolphin graph and study which nodes (if any) are highly central according to the three centralities.
