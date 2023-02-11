# OTT-Market-Segmentation-using-Clustering

## Introduction
The growth of Over-the-Top (OTT) streaming services has sparked an interest in understanding the relationship between the OTT market characteristics and the demographics of viewers. This project aimed to analyze two datasets related to the OTT market in the US to determine this relationship. The first dataset, <b>OTT_Market_Data.xlsx</b>, contains information about the OTT market and the second dataset, <b>OTT_Viewer_Data.xlsx</b>, includes information about viewer demographics.

## Data Preprocessing
In order to determine the relationship between the market and viewer characteristics, a combination of clustering and aggregation techniques were applied to the two datasets. The first step was to apply KNN clustering to the <b>OTT_Market_Data.xlsx</b> dataset, with each type using a different combination of continuous dimensions. The best analysis was determined to be the final analysis, which used viewers and media channels.

## Clustering Algorithms
The final clustering was performed using three different algorithms: <br>

<b> Agglomerative Clustering : </b> Agglomerative Clustering is a bottom-up approach to clustering where each data point is treated as an individual cluster and then merged into bigger clusters iteratively until a stopping criterion is met. 
```
start with each data point being a separate cluster
repeat until the stopping criterion is met:
  find the closest pair of clusters
  merge the two closest clusters into one
end
```
<br>

<b> Birch Clustering : </b> Birch Clustering is an incremental clustering algorithm that builds a tree-based representation of the data, called the CF Tree. The tree is constructed incrementally, with each data point being assigned to a leaf node. If a leaf node exceeds a certain threshold, it is split into two child nodes.

```
create an empty CF Tree
for each data point x:
  navigate the CF Tree to find the closest leaf node
  if the distance between x and the closest node is larger than a threshold:
    create a new leaf node for x
  otherwise:
    add x to the closest leaf node
  if the number of points in the leaf node exceeds a threshold:
    split the leaf node into two child nodes
end
```
<br>
<b> Spectral Clustering : </b> Spectral Clustering is a graph-based clustering algorithm that uses the eigenvectors of the graph Laplacian matrix to find clusters in the data. The algorithm starts by constructing a similarity graph between the data points and then computes the eigenvectors of the Laplacian matrix of the graph. Finally, the data points are assigned to clusters based on their eigenvector values. 

```
construct the similarity graph between data points
compute the eigenvectors of the graph Laplacian matrix
assign data points to clusters based on their eigenvector values
```

<br>
Each algorithm was applied to the combination of viewers and media channels in the OTT_Market_Data.xlsx dataset and the results were compared. The best algorithm was selected based on the <b>elbow method</b>, which is a common technique used in determining the optimal number of clusters.

## Aggregation
Once the best algorithm was selected, an aggregation method was applied to determine the final clusters. The final cluster labels were then applied to the OTT_Viewer_Data.xlsx dataset, which revealed the relationship between OTT market characteristics and viewer demographics in the US.

## Results
The results of this project can be valuable to OTT service providers in understanding the market characteristics and viewer demographics in the US. By understanding this relationship, OTT service providers can target their audience more effectively and improve their offerings to better meet the needs of their customers.

## Conclusion
This project provides a comprehensive analysis of the OTT market in the US and the relationship between market characteristics and viewer demographics. The results of this project can be used as a foundation for further research in the area of OTT market characteristics and viewer demographics.
