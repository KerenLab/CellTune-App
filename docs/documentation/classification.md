---
layout: default
title: Classification
parent: Documentation
nav_order: 10
permalink: /documentation/classification
---

---

## Cell Classification

Cell classification assigns each cell to a cell type or lineage based on its marker expression profile. In CellTune, this is achieved through an active-learning workflow—you iteratively label cells, train supervised models, and refine predictions to rapidly converge on high-quality lineage assignments. This section of the documentation walks you through the classification process and shows how to build, improve, and validate your cell type labels.

Before starting classification you need to have [features calculated (or imported)](/documentation/features) and initial [landmark](/documentation/landmarking) labels in a population set.



