---
layout: default
title: Intro to Gating
parent: Gating
grand_parent: Tutorials
nav_order: 1
permalink: /tutorials/gating/gating-intro
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