---
layout: default
title: Automated Landmarking
parent: Landmarking
grand_parent: Tutorials
nav_order: 2
permalink: /tutorials/landmarking/automated-landmarking
---

---
## Automated Landmarking 

### Automated Landmarking Options 
&nbsp;  

We start by creating a new empty population set for our landmarks. 

Here we gate for CD3+ T cells: CD3 high, CD4 low, CD8 low, & other non-T cell markers low like CD68 for example. 

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/Landmarking_Automated_1.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>


---
### Visualize Automated Landmarks

After creat
<video width="100%" controls>
  <source src="{{ '/assets/tutorials/Landmarking_Automated_View_2.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>


---
### Review Automated Landmarks

We need to verify the automated landmarks by reviewing them.  

From the menu: `Populations -> Review Population Set`  
Make sure 'Automated Landmarks' is also selected as the output set (we are editing the labels of this population set without writing label changes to an additional population set.)


<video width="100%" controls>
  <source src="{{ '/assets/tutorials/Landmarking_Automated_Review_PopulationSetReview.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

> Since we have associated channels to cell types in our CellTypeTable used for the automated landmarking we can use the `Auto Channel Select` option, so the corresponding channels will be visible when we get to the landmark cell (e.g. FOXP3, CD4, and CD3 will be turned on when a Treg landmark is being reviewed).
> Randomizing the order here is not desirable as we want to review each cell type in order (e.g. all the CD8T cells then all the B cells). Randomizing the order is useful when reviewing 

---
