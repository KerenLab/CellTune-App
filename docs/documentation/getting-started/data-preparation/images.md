---
layout: default
title: Images
parent: Data Preparation
grand_parent: Getting Started
nav_order: 1
permalink: /documentation/getting-started/data-preparation/images
has_children: false
---

---

## Format & Organize Images


### Image Formats


---

### Image Organization


---

### Pre-Processing

We highly recommend pre-processing your images to clean out background, noise, and artifacts before using CellTune.  
This will produce cleaner inputs, making it easier to classify (saving you time), and can also reduce image sizes significantly.

**Fluorescence Images** (e.g. CODEX Phenocycler, Lunaphore COMET)
Our lab generally prefers to pre-process fluorescence data by converting each multi-TIFF image into a **single TIFF directory** and then performing **background cleaning with [Ilastik](https://www.ilastik.org/) pixel classifiers** one channel at a time. 

**Mass-Based Images** (e.g. MIBI, IMC)
Our lab generally prefers to pre-process mass-based images using [MAUI (MBI Analysis User Interface)](https://github.com/angelolab/MAUI). 

You can use any pre-processing tools. You just need to make sure that at the end your data is an integer type (uint8 or uint16). 

> Some pre-processing tools convert to float values (e.g. pixels with values like 0.003). ***CellTune does not currently support float  type images.*** You could scale your images and convert to integer by multiplying by a factor. It is important to understand what pre-processing is done and to look at your images before and after any pre-processing to see that you are not losing too much signal (or leaving too much noise). 

---