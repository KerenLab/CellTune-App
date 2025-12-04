---
layout: default
title: Data Exploration
parent: Documentation
nav_order: 7
permalink: /documentation/data-exploration
---

---
## Data Exploration

Data exploration helps you understand channel expression and the underlying expression patterns of cells in your data. With CellTune’s visualization and unsupervised clustering tools, you can quickly identify candidate celltypes or lineages to focus your gating, landmarking, and labeling on. This section covers how to inspect your data before moving into the classification workflow.

### Clustering 
CellTune provides unsupervised clustering to reveal structure in the data and highlight distinct cell populations. The purpose of this step is straightforward: discover the cell types—both expected and novel—examine their expression profiles (e.g., mean cluster expression), and use this information to update your CellTypeTable.

Importantly, the goal is *not* to use these clusters as final classifications (their accuracy is limited), but rather to **identify celltypes present** in the data and, if needed, [sample and review cells from each cluster to establish landmarks](/documentation/landmarking/clustering-based) for initial classification training.


Menu_Plot.png
CD8T_Clustering_View.png




Menu_Clustering.png

Clustering_CD8T_Create_Feature_Group.png
Clustering_CD8T_Dialog.png
Clustering_CD8T_SelectFeatureGroup.png
Clustering_Dialog.png
Clustering_Filter_Populations.png
Clustering_Heatmap.png
Clustering_Heatmap_Dialog.png
Clustering_Visualize.png


Phenotype
Heatmap_CD8T_Phenotype.png
Heatmap_CD8T_Phenotype_Dialog.png




Heatmap_Predictions.png
Heatmap_Predictions_Dialog.png

