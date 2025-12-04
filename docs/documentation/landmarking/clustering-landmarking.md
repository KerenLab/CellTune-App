---
layout: default
title: Clustering-Based
parent: Landmarking
grand_parent: Documentation
nav_order: 3
permalink: /documentation/landmarking/clustering-landmarking
---

---
## Landmarking by Sampling from Clusters

Clustering provides a quick overview of the celltypes and phenotypes present in your dataset and is a useful starting point when you are building or validating your [CellTypeTable](/documentation/getting-started/data-preparation/celltype-table). While clusters are not accurate enough to serve as final classifications, they are very effective for sampling representative cells that can be manually reviewed and used as landmarks for initial training.

In this workflow, you [run clustering](/documentation/data-exploration/initial-clustering), inspect marker expression (e.g., via heatmaps), select clusters enriched for specific lineages, and then sample and review cells to find and confirm true examples of each cell type. These verified and labeled cells form your landmarks, which are essential for the first round of supervised classification.

A detailed, step-by-step tutorial is provided for this [clustering-based landmarking](/tutorials/landmarking/clustering-landmarking) workflow.

