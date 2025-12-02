---
layout: default
title: Labeling Basics
parent: Labeling & Review
grand_parent: Tutorials
nav_order: 1
permalink: /tutorials/labeling-review/labeling
---

---
## Labeling Basics

### Add Labels Manually
&nbsp;  

You can select a cell (`Shift` + `LClick`) and add it to a new population using the (`+`) button in the labeling toolbar or clicking on the population in the population panel at the top right..

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/LabelManually.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

- You can give a cell multiple labels by holding the `Cmd` button while clicking on the populations in the population panel.

&nbsp;  

Next, an example of how you can label many cells quickly by manually by panning and changing channel groups with keyboard shortcuts.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/LabelMultipleCellsPanning.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>


&nbsp;  

Here, we show an example of how you can zoom out to see the whole field-of-view in order to identify cells for manual labeling.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/LabelZoomOutIdentify.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>


--- 
### Clear Labels for a Cell
&nbsp;  

You can clear all the labels for a selected cell using the broom icon in the labeling toolbar.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/LabelClearAll.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

- You can unlabel a cell for a specific population by holding the `Cmd` button while clicking on that population in the population panel.

--- 
### Label as Ambiguous
&nbsp;  

You can label a cell as `Ambiguous` using the corresponding icon in the labeling toolbar.  
Cells labeled as *Ambiguous* are excluded for training.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/LabelClearAll.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

> Labeling a cell as Ambiguous is optional — you can simply skip labeling it during review or remove its label entirely. In all cases, the cell will not be included in training. The Ambiguous label is useful if you want to keep track of uncertain cells and return to them later.
  
- *Note: for ease of use we recommend using our [naming conventions](/documentation/labeling#celltype-name-conventions) for* **Ambiguous**, **Unidentified**, *and* **Garbage** *cell type classes.*


---