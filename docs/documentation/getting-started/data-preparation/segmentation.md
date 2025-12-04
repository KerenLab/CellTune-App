---
layout: default
title: Segmentation
parent: Data Preparation
grand_parent: Getting Started
nav_order: 2
permalink: /documentation/getting-started/data-preparation/segmentation
has_children: false
---

---

## Format & Organize Segmentation
 

### Segmentation Formats

- Segmentation **label images** are required for CellTune. [Pixels values indicate the cell IDs, 0=background.]
- Segmentation should be single TIFF format (2D)
- Segmentation must be the same size as corresponding channel images.
- Data type should be integer type: `uint16` or `uint32`
> (*`int16` and `int32` should also work*)


---

### Segmentation Organization

Segmentation can be stored in a new separate folder, we recommend `/CellTune_Data/{PROJ_NAME}/Segmentations`
- Names should be `{IMAGE_NAME}_segmentation_labels.tif` (e.g. `Control_01_FOV_1_segmentation_labels.tif`)

See [whole slide example in the tutorial](/tutorials/additional-tutorials/whole-slide-example)

If your images are single TIFF directories (like the demo data). Then you can store the segmentations directly in the image folders, named `segmentation_labels.tif` (e.g. `/CellTune_Data/{PROJ_NAME}/Images/Control_01_FOV_1/segmentation_labels.tif`).

---