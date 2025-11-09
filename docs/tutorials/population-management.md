---
layout: default
title: Population Management
parent: Tutorials
nav_order: 4
permalink: /tutorials/population-management
---

---

## Step 5: Create Empty Population Set
&nbsp;  

Create an empty population set. You can add populations to it (e.g., from gating).

<video width="100%" controls>
  <source src="{{ '/assets/tutorial/CreateEmptyPopulationSet.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

---

## Step 6: Gating

### 6A. Gating Basics
&nbsp;  

Select the feature that you want to gate and click **Apply Gate**.  
Shown is an example of gating CD3+ and CD4+ cells.

<video width="100%" controls>
  <source src="{{ '/assets/tutorial/GatingCD3CD4.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

Gating occurs across the entire project currently. (We are adding the capability to limit to the current image).

---

### 6B. Adjust Gating Appearance
&nbsp;  

You can adjust the opacity and whether gated cells are filled in.

<video width="100%" controls>
  <source src="{{ '/assets/tutorial/AdjustGatingOpacity.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

Currently gated cells can only be displayed in the color cyan. (We are adding the capability to edit this).

---

### 6C. Create Population from Gating
&nbsp;  

<video width="100%" controls>
  <source src="{{ '/assets/tutorial/GatingCreatePopulation.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

---

### 6D. Filter Gate by Population
&nbsp;  

You can select populations in the current population set and use them as a filter for your gating.

<video width="100%" controls>
  <source src="{{ '/assets/tutorial/GatingPopulationFilter.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

---

### 6E. Edit Gating Expression
&nbsp;  

You can edit your gating expression to use AND (`&`), OR (`|`), and NOT (`!`) operations.

<video width="100%" controls>
  <source src="{{ '/assets/tutorial/GatingEditExpression.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

By default the gating expression uses AND (`&`) for all compound gates.

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

