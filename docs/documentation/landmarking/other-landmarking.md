---
layout: default
title: Other Landmarking
parent: Landmarking
grand_parent: Documentation
nav_order: 4
permalink: /tutorials/documentation/other-landmarking
---

---
## Other Landmarking Options

### Label Cells Directly
&nbsp;  

If you prefer you can simply manually label cells directly from the images.  

*Reminder:* you need >10 labels per class to start. You can monitor the population counts [From the menu: `Populations -> Population Counts`]

The skills needed to do so are shown in the [manual landmarking](/tutorials/landmarking/manual-landmarking) and [clustering-based landmarking](/tutorials/landmarking/clustering-landmarking) tutorials

- First you need to create an empty Landmarks population set.
- Then select a cell (`Shift` + `LClick`) and add it to a new population using the (`+`) button in the labeling toolbar.
- You can scroll through channel groups while zoomed out to quickly identify areas with candidate cells then zoom in and label.

When you have enough cells for each cell type, we recommend reviewing the cells as was shown in [automated landmarking](/tutorials/landmarking/automated-landmarking).  
You can then proceed to add these labels to a [classifier](/tutorials/classification). 


---

### Import Landmark Cells
&nbsp;  

You can also import labels if you already have some for this datset using the menu `Import -> Populations`.
For landmarking these labels should extremely confident (those generated through clustering-based or other methods are usually not of this quality). You can gate and sample on the imported labels population set like we did for the clusters population set in the [clustering-based landmarking](/tutorials/landmarking/clustering-landmarking) tutorial. 

You don't need a ton of labels to start training, so recommend sampling these down if you have a lot. 

We always recommend reviewing the landmark cell labels as was shown in [automated landmarking](/tutorials/landmarking/automated-landmarking).  
It will not take very long to verify and can save you significant time compared to training with incorrect labels.

---
