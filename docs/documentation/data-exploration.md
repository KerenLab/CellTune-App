---
layout: default
title: Data Exploration
parent: Documentation
nav_order: 7
permalink: /documentation/data-exploration
has_children: true
---

---
## Data Exploration

Data exploration helps you understand channel expression and the underlying expression patterns of cells in your data. With CellTune’s visualization and unsupervised clustering tools, you can quickly identify candidate celltypes or lineages to focus your gating, landmarking, and labeling on. This section covers how to inspect your data before moving into the classification workflow.

## Initial Clustering 
CellTune provides unsupervised clustering to reveal structure in the data and highlight distinct cell populations. The purpose of this step is straightforward: discover the cell types—both expected and novel—examine their expression profiles (e.g., mean cluster expression), and use this information to update your CellTypeTable.

Importantly, the goal is *not* to use these clusters as final classifications (their accuracy is limited), but rather to **identify celltypes present** in the data and, if needed, [sample and review cells from each cluster to establish landmarks](/documentation/landmarking/clustering-based) for initial classification training.

CellTune uses flowSOM (Self-organized maps) unsupervised clustering:
- description
- The number of clusters is determined by the clustering parameters (xdim * ydim). 


### Run Clustering
Select clustering through the classification menu bar:
![Menu_Clustering](/assets/documentation/Menu_Clustering.png){: width="35%"}  

A dialog will open where you can adjust the clustering settings:
![Clustering_Dialog](/assets/documentation/Clustering_Dialog.png){: width="35%"}  

If you currently have populations, you can click on the radio button for `Select Populations` to perform clustering to generate subgroups of populations, [see example below](#cluster-subpopulations).

- You need to select features - as seen previously in the hover legend, it is recommended to create a `Lineage` feature group and select it here.
- Can adjust the xdim and ydim cluster parameters - the number of clusters shown below will update if you adjust them. 
- Give a name for your clustering population set (Here we chose `Clusters`)

Click `OK` and clustering will run.
Next, the clusters will be loaded into the Populations Panel and you can visualize them:

![Clustering_Visualize](/assets/documentation/Clustering_Visualize.png){: width="100%"}  


### Plot Heatmap
Aside from visualizing clusters in the viewer, it is helpful to look at a heatmap of mean expression of the cells in each cluster.

To generate this heatmap go to the `Plot` menu and select `Plot Expression`:
![Menu_Plot](/assets/documentation/Menu_Plot.png){: width="35%"}  

The heatmap dialog will appear: 

![Clustering_Heatmap_Dialog](/assets/documentation/Clustering_Heatmap_Dialog.png){: width="55%"}  

You can select several options:
- Included Features 
- Cluster average statistic: mean or median 
- Clustering of populations & features
- Normalization
- Colormap

Then click `Plot` and your heatmap will appear!

![Clustering_Heatmap](/assets/documentation/Clustering_Heatmap.png){: width="75%"}  



### Subpopulation Clustering
You can select a subset of populations and cluster them alone. 
For example, you can gate on CD8 and create a population of CD8+ cells, then cluster those cells only. 
This can be helpful to see subsets of populations that are not seen when clustering all of the cells together.





Clustering_CD8T_Create_Feature_Group.png
Clustering_CD8T_Dialog.png
Clustering_CD8T_SelectFeatureGroup.png
Clustering_Filter_Populations.png


CD8T_Clustering_View.png

Phenotype
Heatmap_CD8T_Phenotype.png
Heatmap_CD8T_Phenotype_Dialog.png


Heatmap_Predictions.png
Heatmap_Predictions_Dialog.png

