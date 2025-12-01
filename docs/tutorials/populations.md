---
layout: default
title: Populations
parent: Tutorials
nav_order: 4
permalink: /tutorials/populations
---

---
## Populations 


## Step 5: Create Empty Population Set
&nbsp;  

Create an empty population set. You can add populations to it (e.g., from gating).

<video width="100%" controls>
  <source src="{{ '/assets/tutorial/CreateEmptyPopulationSet.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

---



## Step 7: Import Population Set
&nbsp;  

Population sets can be imported from files (CSV). Columns should be `(image, cellID, class)`.  
Here we are importing labels to be used for training a classifier later. We can also import `PopulationSetInfo`, which includes colors, channels, and definitions for cell types (useful later).

<video width="100%" controls>
  <source src="{{ '/assets/tutorial/ImportPopulationSet&Info.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

A cell can belong to multiple populations. For population sets that are used as labels for training classifiers we encourage limiting a cell to one population.

---