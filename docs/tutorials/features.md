---
layout: default
title: Features
parent: Tutorials
nav_order: 3
permalink: /tutorials/features
---

---

## Features

### Calculate Features
&nbsp;  

Features must be computed or imported in order to enable gating, classification, and cell expression hover info.
Select `Calculate -> Cell Features` in the menu.
Then select channels (by default includes all)

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/CalculateFeatures.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>
<br>

- By default, all channels are selected. We don't usually change this.
- The default transformation is arcsinh. By default we use a factor of **0.1** for fluorescence imaging and we use **100** for mass-based imaging (e.g. MIBI) as is shown in the tutorial.
- You need to set the **pixel size** here (microns per pixel) for your images. For our images it is 0.4. In the very near future we will read this directly from the image data when setting up the project. 
- You can adjust the **number of cores** used for processing here. The optimal value depends on your system resources and image sizes. Using too many cores with large images can exhaust your RAM and cause processing to fail; if that happens, try lowering this number. We are working on an automatic method to choose an appropriate number of cores for you.
- Advanced settings are accessible like changing the distances from which to calculate the erode, dilate, and environment spatial features. 
<br><br>
For more details see the [features documentation](/documentation/features).


---

### Import Features
&nbsp;  

Features can be alternatively be imported via a cellTable (CSV or Parquet file).  
The cellTable should have the columns: `(image, cellID)` or `(fov, cellID)`.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/Import_Cell_Features.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

---

### Hover Legend Features
&nbsp;  

Select features that will be displayed while hovering.


<video width="100%" controls>
  <source src="{{ '/assets/tutorials/HoverFeaturesSelection.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

It is recommended to [create a `Lineage` feature group](#create-feature-group) and select it. 


By default the features will be sorted as you hover of them.
Here, we show how you can turn this setting off:

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/HoverScanningChangeFilter.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>


For example you can filter down to a few features without sorting and then by hovering you can quickly compare how the values change.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/HoverFilter3Features.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

> For cell classification it is most useful to sort the features and see what is the top expressing features. These features are most informative with [clean data](/documentation/getting-started/data-preparation/images#pre-processing) and with the appropriate [transformation factor](/documentation/features) for your data. 

---

### Create Feature Group
&nbsp;  

Create a feature group that can be easily selected in different contexts (plotting, hovering, etc.).
The `Default` feature group is the mean for all channels on each cell.
Here we create a `Lineage` feature group.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/Features_CreateFeatureGroup.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

--- 






