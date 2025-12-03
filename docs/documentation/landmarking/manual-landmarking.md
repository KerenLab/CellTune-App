---
layout: default
title: Manual Landmarking
parent: Landmarking
grand_parent: Documentation
nav_order: 1
permalink: /documentation/landmarking/manual-landmarking
---

---
## Manual Landmark Gating 

When manually gating we want to set high positive thresholds for the proteins that must be expressed (*PrimaryMarkers*) and low negative thresholds for the proteins that should not be expressed. 
CD4T Example:
- Must be positive for CD3 and CD4 (*remember myeloid cells also can express CD4!*). These are what we define as `PrimaryMarkers` in our CellTypeTable. ***So we set high positive gates for CD3 and CD4.***
- Must be negative for CD8, FOXP3, CD20, CD68, IgA, Mucin, CHGA, etc ... Of course there will be many CD4T cells with spillover of these markers from neighboring cells, but our landmarks are the cells that do not. ***So we set low negative gates against CD8, FOXP3, etc.***
- Could be positive for CD45, CD103, CD38, etc. These are what we define as `TertiaryMarkers` (could be positive or negative). ***So we do not set any gates for these.***
> Consider if a cell was CD3+CD4+ & CD45-, how should it be classified? If the answer is still CD4T then CD45 is not a `PrimaryMarker`. 
- Some proteins stain the tissue broadly and all cells have some signal of expression from them. For example Collagen. In this case we include this marker as a `TertiaryMarker` and do not set gates against it (or set not too low negative gates against it.)


You can keep track of how many cells are still passing all of your gates in the gating histogram window.

After all these gates you will be left with a subset of cells that are highly likely (>90%) to be correctly classified. We still sample and review them, to be 100% certain, and since we do not need all of these. 

[An example of manual landmarking](/tutorial/landmarking/manual-landmarking) is shown in the tutorial.


### Which proteins are expressed on a cell?
If you are not sure which proteins are generally expressed for a given celltype in your data, you can do an [initial data exploration / clustering](/documentation/data-exploration) or you can gate, create a population from the gate, and then [plot the mean expression] of the gated cells across all lineage markers.

### Using Neighbor Features
Gating on neighbor features can be helpful to isolate very confident cells.
For example, cells which are high for `CD163` and low for `CD163__Mean__Cell__NeighborMax`, we can be confident that the CD163 signal is coming from the cell itself (unless there is very bad segmentation). 

An [example of gating with neighbor features](/tutorials/gating/advanced-gating#using-neighbor-features-for-gating) is shown in the tutorial. 