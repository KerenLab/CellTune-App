---
layout: default
title: Whole Slide Example
parent: Additional Tutorials
grand_parent: Tutorials
nav_order: 1
permalink: /tutorials/additional-tutorials/whole-slide-example
---

---

## Whole Slide Example  
[Demo Videos Below](#whole-slide-demo-videos)
&nbsp;

Here we will show how to import **OME-TIFF whole-slide images** into CellTune.  
The same folder organization applies to **QPTIFF** data as well.
For more info see the [data-preparation documentation](/documentation/getting-started/data-preparation) 

&nbsp;

### 1. Create your project folder
Inside your `CellTune_Store/CellTune_Data` directory, create a folder for your project, for example:

`CellTune_Store/CellTune_Data/Melanoma_Nov0725`

Within this folder, create the following subfolders:

- `Images/`
- `Segmentations/`
- `Tables/`

&nbsp;

### 2. [Optional] Prepare your Tables  

Create your tables:
- `Tables/MarkerTable.csv`
- `Tables/CellTypeTable.csv`

For instructions see documentation for MarkerTable(/documentation/getting-started/data-preparation/marker-table) and CellTypeTable(/documentation/getting-started/data-preparation/celltype-table) preparation.

> You can also place any image/patient metadata tables here for organization. We plan that CellTune will utilize this data in the future.

&nbsp;

### 3. Add your Whole-Slide Images
Organize all OME-TIFF images into the `Images/` directory:
- `Images/WholeSlide1.ome.tiff`
- `Images/WholeSlide2.ome.tiff`
- `...`

&nbsp;
&nbsp;

When prompted in CellTune, create a new project folder `CellTune_Store/**CellTune_Projects**/Melanoma_Nov0725`, and then select this **Images** directory as your image folder.

&nbsp;
&nbsp;



### 4. Add Segmentations (External)
Place the segmentation masks in the `Segmentations/` folder using matching filenames with suffix *'_segmentation_labels.tif'*:

- `Segmentations/WholeSlide1_segmentation_labels.tif`
- `Segmentations/WholeSlide2_segmentation_labels.tif`
- `...`

&nbsp;


### 5. Zarr generation notes
Generating OME-Zarr from large whole-slide images may take a long time, depending on your system resources and drive read/write speed, and it also requires substantial memory. In our initial tests, the most efficient workflow was to **copy the data locally**, run the New Project Setup to generate the Zarrs, and then move or delete the temporary copy afterward.

Ensure you have sufficient RAM (**>16 GB recommended**) and enough local disk space (approximately **2× the size** of the compressed TIFF or OME-TIFF/QPTIFF images) before generating the Zarrs.

We are actively working on improving generation speed and more effective use of remote/networked storage in future releases, as well as the option to **skip Zarr generation entirely** when data is already stored in an efficient format by the user and no editing is planned.

&nbsp;


***Tip:*** Before using CellTune, our lab generally prefers to [**pre-process the data**](/documentation/getting-started/data-preparation/images#pre-processing) by converting each OME-TIFF image into a **single TIFF directory** and performing **background cleaning with [Ilastik](https://www.ilastik.org/) pixel classifiers**. This often produces cleaner inputs, making it easier to classify, and can also reduce image size significantly.
 

---
## Whole Slide Demo Videos

### Start a New Project and Select Images
<video width="100%" controls>
  <source src="{{ '/assets/tutorials/WholeSlideSelectImages.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

--- 
### Select Segmentation from External Directory

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/WholeSlideSelectSegmentation.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

--- 
### Create Project (Generates Zarrs)

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/WholeSlideMonitorZarrProgress.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

--- 
### Adjust Channels

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/WholeSlideAdjustChannels.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

--- 
### Adjust Segmentation Opacity

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/WholeSlideAdjustSegmentationOpacity.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

---

### Zoom & Pan

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/WholeSlideZoomPan.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

--- 

### Calculate Features 

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/WholeSlideCalculateFeaturesDialog.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

--- 
### Gating

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/WholeSlideZoomGating.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>








