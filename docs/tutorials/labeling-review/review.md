---
layout: default
title: Review
parent: Labeling & Review
grand_parent: Tutorials
nav_order: 2
permalink: /tutorials/labeling-review/review
---

---
## Review

Review is where you go through a selected set of cells and confirm or adjust their labels. This step is useful for labeling sampled cells, correcting predictions, inspecting candidate cells from gating, improving the quality of your landmark cells, and more. In the tutorial below, you'll learn see how to use review mode, navigate through the cells, and apply labels efficiently.

For a detailed explanation of how Review works behind the scenes (cell samples, viewing population sets, and output population sets), see the [review documentation](/documentation/review).

### Labeling in Review Mode
&nbsp;  

In *Review Mode* you can navigate through cells with *Next* and *Prev* buttons in the review toolbar or use the keyboard shortcut [`Cmd` + `Left/Right`](/documentation/keyboard-shortcuts).
Cells can be labeled by clicking the buttons in the review toolbar (clicking on a label there will remove other labels).
Cells can also be labeled by clicking on the populations at the top right.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/Labeling1.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

---

### When Both Predictions are Incorrect
As shown above, when reviewing the cells, you see the predictions of the two models and can select one of them by clicking on the button in the review toolbar. 
Sometimes neither prediction is correct. 
Here we show an example where we decided to give the label `Macrophage` even though neither model predicted that.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/Review_Different_Label.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

> This can happen frequently in the first few cycles and then should happen much less later on as the models learn.


### Exit Review and Retrain Classifier
&nbsp;  

When you finish labeling you can exit the review and retrain your classifier. 

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/ExitReviewRetrain.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

- You must exit the review mode to retrain.
- You can retrain at any point, i.e. you don't have to label all of the sampled cells in the review, but if you do retrain you should sample cells again and which will generate a new review. 

--- 


### Label curation outside of ***Review Mode***
&nbsp;  
Labeling in *Review Mode* is most efficient. However you might also want to curate your predictions and add labels outside of review mode.
***Important:*** Keep in mind that if you exit *Review Mode*, labels will not be recorded / copied to the output set 'Labels_Classifier_1' they will only be changed in the visible population set (the predictions). You can still curate & label, by switching the population set before you label. An example is shown in the following clip:

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/Review_Predictions_Change_Label_2.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

Here is another example where we zoom out and hover over a cell with predictions for CD8T and Fibroblast.
It is clearly a CD8T - so we change the population set to 'Labels_Classifier_1' and label it.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/Review_Predictions_Change_Label_3_CD8T.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

--- 

### Review Mode Index Colors

During Review Mode, the color of the cell index (e.g., 3 in 3/2000) provides an immediate indication of how the label in the output population set relates to what you are currently viewing.

For a full explanation of these color indicators, see the [Review Documentation](/documentation/review).

The video below shows an example mismatch:
we exit Review Mode and change a cell’s label in the output set (e.g., Labels_Classifier_1) to `Monocyte`, while the viewing population set shows `Macrophage`.
When returning to Review Mode, the index appears red, indicating the discrepancy.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/Review_Mismatch_Labels.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

---

