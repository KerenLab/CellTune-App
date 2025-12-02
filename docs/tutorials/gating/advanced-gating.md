---
layout: default
title: Advanced Gating
parent: Gating
grand_parent: Tutorials
nav_order: 2
permalink: /tutorials/gating/advanced-gating
---

---
## Advanced Gating


### Edit Gating Expression
&nbsp;  

By default multiple gates will use AND (`&`) operators, but you can edit these to combine gates with AND (`&`), OR (`|`), and NOT (`!`) operators in order to orchestrate complex logic.

CD68 OR CD163:

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/GatingEditExpression.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>


CD68 OR CD163 OR CD206:
<video width="100%" controls>
  <source src="{{ '/assets/tutorials/GatingEditExpression_2.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>


---

### Filter Gate by Population
&nbsp;  

Use existing populations to constrain the scope of a new gate—ideal for refining subsets.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/GatingPopulationsFilter.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>


Below is another example (just for visualization), where we gated CD38+ cells out of CD3+CD4+ T cells adjusting the gating appearance to be transparent and filled:

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/GatingPopulationFilter.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>


--- 

### Sample from Gate for Review
&nbsp;  

Sample all the cells from the Gate for Review.
We want to make sure they are really all expressing the gated markers.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/GatingSamplingReview.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

- Randomize order of the cells otherwise you will have to go through them image by image.
- Automated Channel Selection should be off here. 
- While reviewing, you can adjust the gate if you find an issue, then exit the review, and sample a new review from the new gate.

--- 
### Using Neighbor Features for Gating

It can help in landmarking to isolate some confident cells by manually gating for low Neighbor expression.
Here we are trying to find Endocrine cell (CHGA+ Cells) so we gate for low neighbor expression of CHGA as well as high expression on the cell itself.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/GatingNeighborFeature.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>


--- 

### Create Population from Gating During Review
&nbsp;   

When the sampled cells are all positive (scrolling through at least 30 random cells) then you can create a population from all of these cells. 

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/GatingReviewAddPopulation.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

--- 