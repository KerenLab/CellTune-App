---
layout: default
title: Clustering-Based
parent: Landmarking
grand_parent: Tutorials
nav_order: 3
permalink: /tutorials/landmarking/clustering-landmarking
---


## Landmarking by Sampling from Clusters

Clustering is a fast way to explore your dataset initially and discover broadly what cell types are present.  
It is usually not very accurate when looking at individual cells (that's why we don't just stop there), but it can be effectively used for sampling representative examples for landmarking (these need to be verified manually as shown in the videos below).  
  
This [data exploration](/documentation/data-exploration) is especially useful when you are new to a panel or dataset, in order to help when building the [CellTypeTable](/documentation/getting-started/data-preparation/celltype-table) or to confirm that no major cell types were missed it.  


> *If you know your antibody panel well, we usually recommend setting up the CellTypeTable first and then checking the clustering to see if anything was missing and/or for help with the [`TertiaryMarker`](/documentation/getting-started/data-preparation/#secondary-tertiary-marker-columns) column.*  
  
  
Clustering produces a population set, and from there, you can examine marker expression, select and gate on clusters of interest, and sample cells for landmark review.

---

### Run Clustering

Run clustering on your cells.   
From the menu: `Classification -> Clustering`  
This create a population set. (We set the name as '*Clusters*').  
Each cell receives a cluster label based on expression similarity for the selected features.  

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/Clustering_Run.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

- The number of clusters is determined by the clustering parameters and is shown below them. 
- For further details, including a description of SOM clustering, see the [documentation](/documentation/data-exploration)

---

### Plot Heatmap for Cluster Population Set

In CellTune you can plot a heatmap for any population set.   
From the menu: `Plot -> Plot Expression`  
  
In the context of clustering, this helps us to quickly identify clusters enriched for specific lineages (e.g., CD20-high B cells, tryptase-high mast cells).  

Select the features that will be in the plot either manually or from a pre-existing feature group. 

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/Plot_Clustering_Heatmap.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

> It is recommended to [create a **Lineage** feature group](/tutorials/features/) that you can select for plotting. This group includes the means of lineage markers (and counts for subregions).

---

### Gating on a Single Cluster

After identifying a cluster of interest from the heatmap, we gate that single cluster (here: cluster 99 is a CD20-high cluster). 
We first create an empty 'Landmarks' population set, and then we sample cells from that cluster to find landmark examples for the target cell type ('Bcell').  
 
*(We set 'Landmarks' as the output set for the sampling review - described in the next section)*

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/Clustering_GatingOnCluster_CreateLandmarks_1.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

> By gating for high CD20, we removed cells that were incorrectly included in the cluster. As the CD20 threshold was raised (e.g., CD20 > 2), the cells that dropped out were clearly CD20-negative in the image. There are still some spillover cells remaining (also from other images), and we address those by sampling and review.

---

### Review Sample for Landmarking

We inspect the sampled cells for landmarking in *Review Mode*.  
First we enter *Review Mode* using the review toolbar. 
Next, select the *Review* `Gating_Review_{N}__Bcell_Candidates`.
This brings us to the first cell - the index is shown in the middle of the review toolbar. 
The goal is to identify and label >10 Bcells to use as our landmarks. 

We use the [keyboard shortcuts](/documentation/keyboard-shortcuts) (`Cmd` + `Up/Down`) to very quickly cycle through pre-existing channel groups(/documentation/viewer#create-channel-groups). This helps greatly to check and verify a wide range of channels really fast.


<video width="100%" controls>
  <source src="{{ '/assets/tutorials/Clustering_Review_Sample_Landmarking_2.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

The first few sampled cells were not good landmarks for the `Bcell` class. The second and third cell were both T cells surrounded by B cells (This highlights the major issue with using clustering as your method for classifying your entire dataset). The fourth cell had a lot of overlap with T cell (CD3 expression), so we preferred to skip it. The fifth cell was a good example of a landmark Bcell. We will label it in the following video.

Since there was not already a `Bcell` class we need to create it. With the cell selected we press the `+` button in the labeling toolbar.
Here we can assign the name and color of the new population. **This labels the cell both in the viewed population set ('Clusters') as well as in the output set ('Landmarks').**

Now we can scroll through the sampled cells quickly using the [keyboard shortcuts](/documentation/keyboard-shortcuts) (`Cmd` + `Right`) to go to the next cell. If we identify a Bcell we can click on `Bcell` in the populations panel to label the cell. 

- If a B cell is identified in the crop but it is not the selected cell, we need to select it first in order to label it (`Shift` + `LClick`).
- We can see how many B cells we have labeled using the shortcut (`Cmd` + `P`) - this table is visible towards the end of the video.
[From the menu: *`Populations -> Population Counts`*]

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/Clustering_Review_Sample_Landmarking_3.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>


---

### Gating on Multiple Clusters

Sometimes one biological population is split into multiple clusters.  
Here we select several clusters at once (22 and 76) and sample them together to gather candidate landmark cells (the example shown is for mast cells, which express Tryptase).

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/Clustering_GatingOnClusters_MastCells_Review_Landmarks.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

> Notice the 22nd cell was clearly a Macrophage neighboring a Mast cell, but it was still in the Mast cluster and passed the Tryptase gate due to spillover signal. [*Note:* You could add this cell as a Macrophage label while you are reviewing the Mast cell Landmarks!].

---
