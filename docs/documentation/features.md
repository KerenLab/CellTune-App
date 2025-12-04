---
layout: default
title: Features
parent: Documentation
nav_order: 6
permalink: /documentation/features
---

---

## Features
Before you can begin gating or training models, you need to have cell features. 
CellTune computes a rich set of features for every cell. This section introduces where these features come from, what they represent, and how they integrate into the rest of the workflow.


### CellTune Spatial Features
CellTune performs an expanded feature extraction step, computing many more features than standard approaches to capture spatial expression patterns useful for classification.
Each feature is derived from a channel and can represent single protein expression, protein colocalization, composites of proteins, or subregions. 
*Only protein expression features are required*

Subregion features provide contextual histological information via pixel classifiers (e.g., smooth muscle masks to distinguish fibroblasts from vascular smooth muscle cells).
- These can be manually prepared or generated with pixel classification tools like Ilastik and QuPath.
(*Under development is incorporating all of these into the GUI*) 

For each feature image, CellTune computes four statistical measures—mean, maximum, variance, and pixel count—across distinct spatial compartments: cell center (erode), entire cell, immediate surroundings (dilate), and broader environment. [See our manuscript for more info](/citation).

Optional marker positivity probability features can be computed using a CNN and incorporated.
In total, ~2,000 features per cell are generated depending on the number of channels, then merged into the cell table.


### Calculate Cell Features
To calculate features go to the menu:
&nbsp;
![Menu_CalculateFeatures](/assets/documentation/Menu_CalculateFeatures.png){: width="35%"}  

This will open the dialog where you can select channels to calculate features on, edit transformation factor, image scale, and number of cores to use when processing. 
&nbsp;
![ComputeFeatures_Dialog](/assets/documentation/ComputeFeatures_Dialog.png){: width="35%"}  
&nbsp;
- For the arcsinh transformation factor we typically use 0.1 for fluorescence images (CODEX, COMET) and 100 for mass-based images (MIBI, IMC).
- You need to put the image pixel size in manually at this time
- It is currently recommended to use 16 cores or less for very large images. 

In the advanced features you can control the distance (microns) that erode and dilate features are calculated at:

&nbsp;
![ComputeFeatures_Advanced](/assets/documentation/ComputeFeatures_Advanced.png){: width="35%"}  

Select `OK` to calculate. It will take some time, you should see a progress bar:
&nbsp;
![ComputeFeatures_ProgressStarting](/assets/documentation/ComputeFeatures_ProgressStarting.png){: width="35%"}  
> *Please note- our progress bars are currently being overhauled, so you may encounter the progress not showing updates properly - do not worry it is still working*.
<!-- TODO remove-->

&nbsp;
When finished you will see the following message:
&nbsp;
![ComputeFeatures_Finished](/assets/documentation/ComputeFeatures_Finished.png){: width="35%"}  

&nbsp;
*[See the tutorial for an example](/tutorials/features#calculate-features)*


### Create Feature Group
It is very useful to save a group of features for use in many contexts (e.g. plotting histograms, clustering, hover feature viewing):
![Menu_Create_Feature_Group](/assets/documentation/Menu_Create_Feature_Group.png){: width="35%"}  

We usually save a `Lineage` group of features, which includes the Mean Cell expression for lineage channels 
![Feature_Group_Create_Lineage](/assets/documentation/Feature_Group_Create_Lineage.png){: width="35%"}  


... as well as the Counts Cell features for any important subregions:
![Feature_Group_Create_Regions](/assets/documentation/Feature_Group_Create_Regions.png){: width="35%"}  

Then you can give the feature group a name:
![Feature_Group_Create_Name](/assets/documentation/Feature_Group_Create_Name.png){: width="35%"}  

and finally when done will get the following message:
![ComputeFeatures_Finished](/assets/documentation/ComputeFeatures_Finished.png){: width="35%"}  


*[See the tutorial for an example](/tutorials/features#create-feature-group)*








