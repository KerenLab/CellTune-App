---
layout: default
title: Labeling
parent: Documentation
nav_order: 4
permalink: /documentation/labeling
---

---

## Labeling


### CellType Name Conventions

It is helpful to use concise and consistent names for cell types while doing the classification process, e.g. `CD4T` instead of `CD4+ T`, without spaces, hyphens, special characters (other than underscores).
So we have standardized cell type naming conventions for our lab - feel free to follow or not.  
All the cell types we've used so far can be found in [CellTuneDepot](/celltunedepot).
(Before publication we change all the names at once to make them nice, adding spaces, using superscripts for +, etc).

We also highly encourage following our lab’s conventions for labeling ambiguous and unidentified cells:

- **“Unidentified”** = Cells that are negative for all lineage markers, lineage is unknown. [Unidentified comes up in every project and is always included in the training.]
- **“Garbage”** = Cells that are artifacts (e.g., multi-channel aggregates, overly positive for many markers, or otherwise unusable). [By default Garbage is included in training to find other similar cells, so it should be a recurring staining issue, otherwise filter out from training]
- **“Ambiguous”** or Skip = Cells that are ambiguous due to overlap or segmentation issues should be labeled “Ambiguous” or skipped entirely.

### Labeling by Cell
Requires that a cell is selected
Link to labeling selected cell / create population

Labeling toolbar

### Labeling by Population
There is interest in a mode where the user would be able to select a population for labeling and then all cells clicked on would be assign to that population. E.g. Labeling mode set to population, select CD8T, then every cell clicked on gets labeled as CD8T. It is on our short-list of new features. 

### Other 
Cells can also be assigned to populations through Gating, Automated Landmarking, and 