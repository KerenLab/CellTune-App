---
layout: default
title: Gating
parent: Tutorials
nav_order: 5
permalink: /tutorials/gating
---

---
## Gating Basics


### Applying Gates
&nbsp;  

Select the feature that you want to gate and click **Apply Gate**.  
Shown is an example of gating by CD45+, and then CD3+.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/GatingBasicsCD45CD3.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

- Gating occurs across the entire project currently. (We are adding the capability to limit to the current image).
- If you do not apply the gate, it won't be saved when you change to a new feature.

---

### Clear All Gates
&nbsp;  

Clear the applied gates.


<video width="100%" controls>
  <source src="{{ '/assets/tutorials/GatingClearAllGates.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

- Clearing the gates does not clear population filters ([described later](#filter-gate-by-population)).

---

### Adjust Gating Appearance
&nbsp;  

You can adjust the opacity and whether gated cells are filled in.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/AdjustGatingOpacityFillVisibility.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

*Currently gated cells can only be displayed in the color cyan. (We are adding the capability to edit this).*


You can turn the gating visibility on/off with the eye icon in the gating panel.
<video width="100%" controls>
  <source src="{{ '/assets/tutorials/GatingVisibility.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

> Note that gating can be visible even if the panel is closed.

---

### Filter Features
&nbsp;  

CellTune calculates many features for classification training, but you don't need all of these for gating.
You can limit the features in the dropdown menu using the filter icon.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/GatingFilterFeatures.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

---

### Create Population from Gating
&nbsp;  

You can create a population from your gated cells.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/GatingCreatePopulation_2.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

> When you create a population from gating, a backup copy of that gated population (.csv) will be stored in your project at the path `/Populations/Gating` along with a record of the gating thresholds in a json file (.info). *Note - the [gating expression](#edit-gating-expression) is not currently saved, assumed as all AND operators*


---

### View All Gates
&nbsp;  

View a table of the thresholds applied on the gates.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/GatingViewAllGates.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>


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


### Add a New CellType / Subset an Existing CellType

While reviewing, we identified a subset of Endocrine cells expressing CD56+ as shown:

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/GatingAddNewCellType.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

We want to add this as a new cell type 'Neuroendocrine'.
We need to filter the 'Endocrine' cell type for those expressing any non-negligible amount of CD56 and sample from them for review.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/GatingReviewAddNewCellType.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

- Cells which are negative for CD56 can stay as Endocrine, we **skip** them.
- Cells which are positive for CD56 get **labeled** as Neuroendocrine.
- Cells which are ambiguous, should have their Endocrine label **removed**.
  
***Important***
- If we are doing this during classification cycles review then the number of labels we need to review is low (a subset of the Endocrine labels we have given so far, usually less than 50). 
- We should need gate any other cell types which could have been mislabeled. E.g. Neuron cells (CD56+) should be filtered for any cells that have expression of CHGA+ in order to find other mistakenly misclassified Neuroendocrine cells (before the class existed).
- During Landmarking we only need to get a small amount (>10) of these cells labeled and review that our landmark labels are all correct. There is no need to review ALL of the cells in a large gating sample - just keep going until you have enough. 

 


