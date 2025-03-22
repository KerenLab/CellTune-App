---
layout: home
nav_order: 1
title: Introduction
---

# Welcome to CellTune
&nbsp;
**CellTune** is an interactive software platform for accurate, high-resolution, and efficient cell classification in multiplexed tissue imaging data.

Combining visualization, manual annotation, and human-in-the-loop active learning, CellTune streamlines the labeling process and enhances classification performance. By engaging users with uncertain or ambiguous predictions, the platform maximizes information extracted from expert input and enables the discovery of novel cell types. 

To benchmark CellTune, we created **CellTuneDepot**—the largest fully manually labeled multiplexed imaging dataset to date—comprising over 40,000 cells comprehensively annotated by experts across 30 cell types. In addition, CellTuneDepot contains over 3 million high-quality semi-supervised labels generated with CellTune across a variety of tissues and disease states with accuracy comparable to expert annotation.

Together, CellTune and CellTuneDepot provide a powerful toolkit for classifying cells and accelerating biological discovery in spatial proteomics.


---

## Download CellTune
&nbsp;
Get the latest version of CellTune for your platform:

- [Download for macOS (.dmg)](https://github.com/yuvalbussi/CellTune-App/releases/latest/download/CellTune.dmg)
- [Download for Windows (.exe)](https://github.com/yuvalbussi/CellTune-App/releases/latest/download/CellTune.exe)
- Download for Linux (.AppImage) — *coming soon*

---

## Download CellTuneDepot
&nbsp;
**CellTuneDepot** is a curated collection of multiplexed imaging datasets with expert-validated labels, intended for benchmarking, model training, and reproducible analysis.

- [Download CellTuneDepot (v1.0)](https://github.com/yuvalbussi/CellTune-App/releases/latest/download/CellTuneDepot.zip)

CellTuneDepot is organized into two main sections: *manual labels* and *CellTune-generated high-quality labels*, and further subdivided by dataset.  
Each dataset includes:  
- Multiplexed images
- Segmentation masks
- Channel and cell type metadata
- Population labels
- Cell table containing per-cell mean protein expression

*Datasets associated with unpublished studies will be released upon their publication.*

> See the *Methods* section of our [manuscript](#citation) for more details on all datasets.

---

## Documentation
&nbsp;
Documentation and tutorials are *coming soon*.  
In the meantime, [contact us](#contact) with questions or usage inquiries.

---

## Citation
&nbsp;
If you use CellTune in your research, please cite:

> Bussi, *et al.* CellTune: An integrative software to expedite accurate cell classification in spatial proteomics  
> *Manuscript in preparation* A formal citation and DOI will be provided upon publication.

---

## Contact
&nbsp;
Found a bug, issue, or have a feature request?  
>[Submit an issue on GitHub](https://github.com/KerenLab/CellTune-App/issues)

For other technical questions, issues, or feedback:  [yuval.bussi@weizmann.ac.il](mailto:yuval.bussi@weizmann.ac.il)  
  
For scientific collaborations or inquiries:  [leeat.keren@weizmann.ac.il](mailto:leeat.keren@weizmann.ac.il)  

---

© {{ site.time | date: '%Y' }} Weizmann Institute of Science. All rights reserved.
