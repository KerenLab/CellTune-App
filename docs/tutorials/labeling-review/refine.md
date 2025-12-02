---
layout: default
title: Refining CellTypes
parent: Labeling & Review
grand_parent: Tutorials
nav_order: 3
permalink: /tutorials/labeling-review/refine
---

---
## Refining CellTypes


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
