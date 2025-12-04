---
layout: default
title: Initial Clustering
parent: Data Exploration
grand_parent: Documentation
nav_order: 1
permalink: /documentation/data-exploration/initial-clustering
---

---

## Initial Clustering 
CellTune provides unsupervised clustering to reveal structure in the data and highlight distinct cell populations. The purpose of this step is straightforward: discover the cell types (both expected and novel), examine their expression profiles (e.g., mean cluster expression), and use this information to update your CellTypeTable.

Importantly, the goal is *not* to use initial clusters as final classifications (their accuracy is limited), but rather to **identify celltypes present** in the data and, if needed, [sample and review cells from each cluster to establish landmarks](/documentation/landmarking/clustering-landmarking) for initial classification training.

CellTune uses flowSOM (Self-organized maps) unsupervised clustering.

### Run Clustering
Select clustering through the classification menu bar:

![Menu_Clustering](/assets/documentation/Menu_Clustering.png){: width="45%"}  

A dialog will open where you can adjust the clustering settings:

![Clustering_Dialog](/assets/documentation/Clustering_Dialog.png){: width="35%"}  


- `Select Cells`: If you currently have populations, you can click on the radio button for `Select Populations` to perform clustering to generate subgroups of populations, [see example below](/documentation/data-exploration/phenotype-clustering). Otherwise, click on `All Cells`.
- `Select Features`: Select features that will be used for clustering.  
As seen previously in the hover legend, it is recommended to create a `Lineage` feature group and select it here.
- `Cluster parameters`: Determine the number of clusters (= xdim * ydim). The number of clusters shown below will update if you adjust them. 
- `Population set name`: Give a name for your clustering population set (Here we chose `Clusters`)


Click `OK` and clustering will run.

Next, the clusters will be loaded into the Populations Panel and you can visualize them:

![Clustering_Visualize](/assets/documentation/Clustering_Visualize.png){: width="100%"}  


### Plot Heatmap
Aside from visualizing clusters in the viewer, it is helpful to look at a heatmap of mean expression of the cells in each cluster.

Following the instructions from the [Plot Expression Documentation](/documentation/data-exploration/plot-expression)
You can generate a heatmap of mean cluster expression of the lineage markers: 

![Clustering_Heatmap](/assets/documentation/Clustering_Heatmap.png){: width="75%"}  

This heatmap can be utilized in several ways:
- As a guide for filling in the CellTypeTable and verifying that you didn't miss any celltypes.
- Inspecting which proteins are often co-expressed on cells by following the hierarchical clustering. This can lead to new insights into your specific dataset.
- Selecting clusters to sample from for landmarking specific celltypes. See [clustering-based landmarking tutorial](/tutorials/landmarking/clustering-landmarking).



