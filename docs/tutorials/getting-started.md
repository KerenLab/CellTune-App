---
layout: default
title: Getting Started
parent: Tutorials
nav_order: 1
permalink: /tutorials/getting-started
---

If you haven’t already installed the CellTune software, please start with the [Download & Install page](/download) before continuing.

---

## Step 1: Download Demo Data
&nbsp;  
[Download images and tables for the tutorial](https://github.com/KerenLab/CellTune-App/releases/download/v0.2.2/CellTune_Demo_Data.zip)

After downloading, unzip the folder.  
You can extract it to your **Downloads** folder or create a dedicated folder such as `CellTune_Data` in your **Documents**.

![Demo Data Folder Contents]({{ '/assets/tutorial/demo_folder.png' | relative_url }})

---

### Demo Data Contents

The demo dataset included with CellTune provides a complete example of spatial proteomics analysis using multiplexed tissue images from the study:
[Azulay et al. “A spatial atlas of human gastrointestinal acute GVHD reveals epithelial and immune dynamics underlying disease pathophysiology.” Science Translational Medicine 17.823 (2025)](https://www.science.org/doi/full/10.1126/scitranslmed.adu6032).  
  
It consists of MIBI (Multiplexed Ion Beam Imaging) data from duodenum and colon biopsies collected from GVHD patients and matched controls, acquired at 0.4 µm/pixel resolution and exported as 8-bit (0–255) single TIFF images.  
  
Preprocessing followed the MAUI pipeline (Baranski et al., 2021), including background subtraction, noise removal, and aggregate filtering. Segmentation was performed using Mesmer (Greenwald et al., 2022) via the ark-analysis pipeline, using a two-pass strategy designed to better capture goblet cells.  For further details, see the methods section of the manuscript.

### `CellTune_Demo_Data/`

- `cellTable_features_calculated.parquet`  
  Pre-computed single-cell features, including intensity, morphology, and spatial statistics.

- `Labels.csv`  
  Cell-level annotations for training and evaluation.

- `PopulationSetInfo.csv`  
  Metadata describing the populations (cell types).

- `Images/`  
  Contains all image data and segmentations used in the tutorial.

### `Images/`

This folder contains **75 subfolders**, each corresponding to a single field of view (FOV) from either control or GVHD tissue:

- `Control_01_FOV_1`, `Control_01_FOV_2`, ..., `GVHD_03_FOV_2`, etc.

&nbsp;  

Each Image (FOV) folder includes:

- **Protein (Marker) Channels**  
  Single-channel grayscale `.tif` images (e.g., `CD3.tif`, `CD4.tif`, `CD8.tif`, `FOXP3.tif`, etc.) representing individual protein markers.

- **Additional Feature Channels**  
  Folders may also include:
  - Subregion masks (e.g., epithelium, muscle, vasculature)
  - Composite or colocalization images (combining multiple marker channels) used for feature extraction 

- **Segmentation Files**  
  - `segmentation_labels.tiff`: Cell instance segmentation image.  
    Each pixel is labeled with a **unique cell ID**, with background as `0`.
  - `segmentation_borders.tiff`: Outlines of segmented cell borders (purely for visualization).

Each FOV in this dataset has 73 channel files + 2 segmentation files.

![Single Image Folder Contents]({{ '/assets/tutorial/single_image_folder.png' | relative_url }})
&nbsp;  

These files will be loaded directly into CellTune when starting a new project.

---

## Step 2: New Project Setup
&nbsp;  

Create a new project using the demo data:

<video width="100%" controls>
  <source src="{{ '/assets/tutorial/NewProjectSetup.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

