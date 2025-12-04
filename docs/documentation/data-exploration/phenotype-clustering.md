---
layout: default
title: Phenotype Clustering
parent: Data Exploration
grand_parent: Documentation
nav_order: 3
permalink: /documentation/data-exploration/phenotype-clustering
---

---
## Phenotyping

In CellTune, we distinguish cell types from phenotypes as follows:

- CellTypes represent lineage or identity (e.g., T cells, macrophages, fibroblasts). These don't typically change for a cell. 

- Phenotypes represent state, function, or activation within a given cell type (e.g., exhausted CD8 T cells, proliferating tumor cells, etc).

Today, the state-of-the-art approach to study phenotypes is to cluster cells within each cell type and interpret those subclusters as phenotype subtypes - the following subsection shows how to do that clustering in CellTune.

### Phenotype Clustering (Subpopulations)

You can select a subset of populations and cluster them alone.
You can generate the population you want to 
For example, you can gate on CD8 and create a population of CD8+ cells, then cluster those cells only. 
This can be helpful to see subsets of populations that are not seen when clustering all of the cells together.

Typically we plot an expression heatmap of our current populations including all markers to identify which are the relevant functional markers for a specific celltype.

Then we create a feature group for each celltype:
![Clustering_CD8T_Create_Feature_Group](/assets/documentation/Clustering_CD8T_Create_Feature_Group.png){: width="55%"}  

Next we open the clustering dialog and filter the populations for the population of interest (here it is CD8T):

![Clustering_Filter_Populations](/assets/documentation/Clustering_Filter_Populations.png){: width="30%"}  

 and select that feature group.

![Clustering_CD8T_Dialog](/assets/documentation/Clustering_CD8T_Dialog.png){: width="30%"}  

We give our clustering population set a name `CD8T_Clusters` and click `OK` to run the clustering.

Then your clusters will be generated and open in the Populations Panel.
You can then view your CD8T clusters by hiding the channels:
![CD8T_Clustering_View](/assets/documentation/CD8T_Clustering_View.png){: width="100%"}  


Next you can plot a heatmap of expression of the CD8T clusters.
Select the `CD8T_Phenotype` feature group in the heatmap dialog:

![Heatmap_CD8T_Phenotype_Dialog](/assets/documentation/Heatmap_CD8T_Phenotype_Dialog.png){: width="100%"}  


![Heatmap_CD8T_Phenotype](/assets/documentation/Heatmap_CD8T_Phenotype.png){: width="100%"}  

- You can go through these clusters and give them names. (*Under development*)
- You can also [export these populations](/documentation/export/populations) for further downstream analysis. 








