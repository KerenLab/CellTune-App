---
layout: default
title: Landmarking
parent: Tutorials
nav_order: 6
permalink: /tutorials/landmarking
---

---
## Landmarking
<br>
Landmarking is the process of assigning trusted cell-type labels to a small subset of cells in your dataset. 
<br>

These **landmark cell labels** provide the initial supervision that CellTune uses **before you can train** any classifiers. 
<br> 

Each cell type should be represented. In practice, you need to label **at least 10 cells per cell type** (aim for 20 each) so that CellTune has enough examples to start learning. 
<br> 

Landmarking can be performed using either manual, automated/semi-automated supervised, or clustering-based approaches, or a combination of them.
<br>

Once you have **landmark labels**, you can proceed to the [classification](/tutorials/classification) tutorial.