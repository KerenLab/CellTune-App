---
layout: default
title: Review & Curation
parent: Documentation
nav_order: 9
permalink: /documentation/review
---

---
## Review & Curation


### CellTune Review
Review is the step where you go through a curated list of cells—one by one—and confirm, correct, or assign their cell type labels.
It is designed to help you quickly produce high-quality labeled data for training or refinement.

A CellTune Review has three key components:

1. A cell sample
This is the specific list of cells you will inspect during the review.
Examples: “CD8T candidates,” “cluster 7 cells,” “classifier predictions.”

2. A viewing population set
This determines what you see while reviewing—e.g., the population set containing classifier predictions or landmarks that provide context.
It controls visibility, colors, and optional auto-channel selection.

3. An output population set
This is where the labels you assign during review are saved.
It can be the same as the viewing population set (e.g., reviewing and updating “Landmarks”), or a separate one (e.g., reviewing classifier predictions and writing results into “Labels_Classifier_1”).

In many cases, the viewing and output population sets are the same—for example, when reviewing a landmark set you are refining.

In short: Review = go through selected cells → inspect them with the right context → assign or correct their labels → write the labels to an output population set along the way.


### Review Mode Index Colors

During Review Mode, each cell you navigate to is shown with an index (e.g., 3 in 3/2000).
The color of this index provides an immediate indication of how the label in the output population set relates to what you are currently viewing.

**Color Meaning**
- Green — The label in the output population set matches the label/prediction being viewed.
- Red — The label in the output population set does not match the label/prediction being viewed.
- White — The cell has no label in the output population set, or you are currently viewing the output set itself.
> (When the viewing set and output set are the same, all cells appear white because there is no comparison being made.)

**Why mismatches occur**

Label mismatches typically arise when:
- A label is manually changed outside Review Mode (e.g., editing the output population set directly),
- The viewing population set shows predictions from a classifier while the output set contains edited or corrected labels, or
- The viewing and output sets represent different stages of labeling (e.g., gating candidates vs. curated labels).

These indicators help highlight disagreements between predicted and assigned labels, making it easy to spot inconsistencies that may need further review.

[See the example in the tutorial](/tutorial/labeling-review/review#review-mode-index-colors)
