---
layout: default
title: Advanced Gating Tips
parent: Population Management
grand_parent: Tutorials
nav_order: 6
permalink: /tutorials/population-management/advanced-gating
---

---

## 6C. Create Population from Gating
&nbsp;  

Turn a finished gate into a reusable population for downstream analysis.

<video width="100%" controls>
  <source src="{{ '/assets/tutorial/GatingCreatePopulation.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

> **Tip:** Name populations with a prefix (for example, `Gate_`) so they sort together in long lists.

---

## 6D. Filter Gate by Population
&nbsp;  

Use existing populations to constrain the scope of a new gate—ideal for refining subsets or comparing phenotypes.

<video width="100%" controls>
  <source src="{{ '/assets/tutorial/GatingPopulationFilter.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

- Activate multiple filters to intersect prior annotations and focus on difficult regions.  
- Save filtered results as new populations to build hierarchical classifications.

---

## 6E. Edit Gating Expression
&nbsp;  

Combine gates with AND (`&`), OR (`|`), and NOT (`!`) operators to orchestrate complex logic.

<video width="100%" controls>
  <source src="{{ '/assets/tutorial/GatingEditExpression.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

- Parentheses control precedence—use them liberally for clarity.  
- Keep frequently used expressions in a text snippet library so you can paste and adapt them quickly.  
- When experimenting, duplicate the original gate first so you always have a clean baseline.

---

## 6F. Iterate Quickly

- **Keyboard navigation:** Arrow keys cycle through saved populations and gates without reaching for the mouse.  
- **Opacity presets:** Store preferred segmentation/gating opacity combinations to maintain visual context while iterating.  
- **Versioning:** Export populations at milestones (e.g., `Gating_v1.csv`) so you can roll back if a later edit overfits.

---

Need a recap of the fundamentals? Return to [Population Management](/tutorials/population-management) for the core workflow. Once you are comfortable, keep this page open as a reference while you fine-tune gates across projects.

