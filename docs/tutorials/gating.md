---
layout: default
title: Gating
parent: Tutorials
nav_order: 5
permalink: /tutorials/gating
---

---
## Gating 


### Gating Basics
&nbsp;  

Select the feature that you want to gate and click **Apply Gate**.  
Shown is an example of gating CD3+ and CD4+ cells.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/GatingCD3CD4.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

Gating occurs across the entire project currently. (We are adding the capability to limit to the current image).

---

### Adjust Gating Appearance
&nbsp;  

You can adjust the opacity and whether gated cells are filled in.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/AdjustGatingOpacityFillVisibility.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

*Currently gated cells can only be displayed in the color cyan. (We are adding the capability to edit this).*

---


### Create Population from Gating
&nbsp;  

Turn a finished gate into a reusable population for downstream analysis.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/GatingCreatePopulation.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

> **Tip:** Name populations with a prefix (for example, `Gate_`) so they sort together in long lists.

---

### Filter Gate by Population
&nbsp;  

Use existing populations to constrain the scope of a new gate—ideal for refining subsets or comparing phenotypes.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/GatingPopulationFilter.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

- Activate multiple filters to intersect prior annotations and focus on difficult regions.  
- Save filtered results as new populations to build hierarchical classifications.

---

### Edit Gating Expression
&nbsp;  

Combine gates with AND (`&`), OR (`|`), and NOT (`!`) operators to orchestrate complex logic.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/GatingEditExpression.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

- Parentheses control precedence—use them liberally for clarity.  
- Keep frequently used expressions in a text snippet library so you can paste and adapt them quickly.  
- When experimenting, duplicate the original gate first so you always have a clean baseline.

---

