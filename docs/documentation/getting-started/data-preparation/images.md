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
CellTune supports loading images from both non-pyramidal and pyramidal formats.

**Non-pyramidal formats**
- Single-channel TIFFs
- Multi-channel TIFF stacks

**Pyramidal formats**
- OME-TIFF
- QPTIFF
- OME-ZARR / ZARR

Most other multiplexed imaging file types can be converted into OME-Zarr using [BioFormats2Raw](https://github.com/glencoesoftware/bioformats2raw), after which CellTune can process them directly.


***ZARR Generation (Current Behavior)***

To get CellTune out faster, CellTune currently converts all supported image formats into internal Zarr stores.
This ensures consistent handling across formats and enables fast region-based access during visualization and feature computation.

*Note: In upcoming versions, Zarr conversion will be optional and skipped when not needed (e.g., native high-quality Zarr or pyramidal formats, or small images). We are working on these checks and optimizations to speed up project setup and minimize disk usage.*


If you have issues with your image format please [contact us](/contact).

---

### Image Organization
Organizing your data cleanly ensures smooth loading, consistent project structure, and portable sharing.

You can load images from any directory, but for convenience and portability we recommend placing them under:

`CellTune_Store/CellTune_Data/{PROJ_NAME}/Images/`

See [Project Documentation](/documentation/projects)



1. Single-TIFF Folder Layout (one TIFF per channel)  

		CellTune_Data/{PROJ_NAME}/Images/
			{IMAGE_NAME_1}/
				channel_1.tif
				channel_2.tif
				...
			{IMAGE_NAME_2}/
				channel_1.tif
				channel_2.tif
				...
	
2. Multi-TIFF / Whole-Slide Formats  

		CellTune_Data/{PROJ_NAME}/Images/
			{IMAGE_NAME_1}.ome.tif
			{IMAGE_NAME_2}.ome.tif
			...
	

**Segmentation labels** 

The segmentation labels should be stored in a separate Segmentations folder.

	CellTune_Data/{PROJ_NAME}/Segmentations/
		{IMAGE_NAME_1}_segmentation_labels.tif
		{IMAGE_NAME_2}_segmentation_labels.tif
		...
	
OR can be inside the Single-TIFF directories with the channels (call them segmentation_labels.tif).
	
See [Segmentation Documentation](/documentation/getting-started/data-preparation/segmentation).


--- 
### How CellTune Handles Images and Zarr Creation

When you create a project, CellTune links (not copies) these image files into the project’s internal `Images/`  directory, allowing multiple projects to reference the same initial images. For each project, it currently makes a copy for its internal Zarr store.

Initial Zarr generation will be significantly slower on remote file systems due to high I/O latency.
We recommend storing data in a dedicated project directory under `CellTune_Data/`.

**Recommended Workflow for Remote Data** 

If possible:
- Copy the image directory locally.
- Create the new CellTune project (the Zarr will be generated from the local files).
- To free space manually delete the local copy and links (`CellTune_Projects/{PROJ_NAME}/Images/Input/`) once the project is created.

*Because CellTune generates internal Zarrs, the temporary local copy and links do not need to be kept after you start your project.*

---

### Pre-Processing

We highly recommend pre-processing your images to clean out background, noise, and artifacts before using CellTune.  
This will produce cleaner inputs, making it easier to classify (saving you time), and can also reduce image sizes significantly.

**Fluorescence Images** (e.g. CODEX Phenocycler, Lunaphore COMET)

Our lab generally prefers to pre-process fluorescence data by converting each multi-TIFF image into a **single TIFF directory** and then performing **background cleaning with [Ilastik](https://www.ilastik.org/) pixel classifiers** one channel at a time. 

**Mass-Based Images** (e.g. MIBI, IMC)

Our lab generally prefers to pre-process mass-based images using [MAUI (MBI Analysis User Interface)](https://github.com/angelolab/MAUI). 

You can use any pre-processing tools. You just need to make sure that at the end your data is an integer type (`uint8` or `uint16`). 

> Some pre-processing tools convert to float values (e.g. pixels with values like 0.003). ***CellTune does not currently support float  type images.*** You could scale your images and convert to integer by multiplying by a factor. It is important to understand what pre-processing is done and to look at your images before and after any pre-processing to see that you are not losing too much signal (or leaving too much noise). 

---