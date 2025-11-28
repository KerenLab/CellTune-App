---
layout: home
nav_order: 5
title: CellTuneDepot
---

## CellTuneDepot
&nbsp;  
**CellTuneDepot** is a curated collection of multiplexed imaging datasets with expert-validated labels, intended for benchmarking, model training, and reproducible analysis.

- [Download v0.2](https://www.dropbox.com/scl/fi/s5mna64yf1y55fj8u2b8t/CellTuneDepot.zip?rlkey=itzwc0fued7vbkcc4wfzrkazc&dl=1) (~5 GB ZIP)

CellTuneDepot is organized into two main sections:

1. **Manual Labels**

   - Fully manually labeled crops/images.

2. **High-Quality Labels**

   - Semi-supervised labels generated with CellTune for entire datasets.

  
Each section is then further subdivided by dataset.  
  
&nbsp;  

### Dataset Composition  

Each dataset includes:

#### 1. **Images Folder**

- **Structure**: Contains subfolders for each image, aka Field of View (FOV).
- **Contents**: Each image subfolder includes:
  - ~40+ TIFF images representing various biological markers.
  - **Segmentation labels image** ('segmentation_labels') for delineating individual cells.
 
#### 2. **Tables Folder**

- **Structure**: Contains CSV files with key data annotations and features.
- **Contents**:
  - **Channels.csv**: List of channels in the dataset with their expected expression cell type or function (Expected_Expression)  
  - **CellTypes.csv**: List of cell types in the dataset with their expression definition (PrimaryMarker)  
  - **Labels.csv**: Table of manual cell labels. Columns= (image, cellID, class). [Manual Labels Datasets Only]
  - **Populations.csv**: Table of cell classification labels for all cells. Columns= (image, cellID, class). [High-Quality Labels Datasets Only]
  - **CellTable.csv**: Mean expression of each protein channel on all the cells in the dataset. [High-Quality Labels Datasets Only]

  

&nbsp;  

### Cell Types

**'CellTypes_ALL.csv'** contains a list of all cell types across datasets and the expression used to define them (PrimaryMarker).


&nbsp;  


  
*Datasets associated with unpublished studies will be released upon publication of their respective manuscripts.*

> See the *Methods* section of our [manuscript](citation) for more details on all datasets.  
  
&nbsp;  

---

© {{ site.time | date: '%Y' }} Weizmann Institute of Science. All rights reserved. [License](/license/)
