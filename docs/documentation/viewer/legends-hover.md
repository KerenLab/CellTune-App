---
layout: default
title: Legends & Hover
parent: Viewer & Interface
grand_parent: Documentation
nav_order: 2
permalink: /documentation/viewer/legends-hover
---

---

## Viewer Legends & Hover Functionality
&nbsp; 

Legends are an important 

### Turning the Legend On/Off

Legend can be turned on/off from the menu or with the keyboard shortcut `Cmd + L`.
![Menu_Legend](/assets/documentation/Menu_Legend.png)


### Including Channels, Cell Info, & Cell Features in the Legend
The legend shows which channels are on:
![Legend_1](/assets/documentation/Legend_1.png)


You can turned off cell info inclusion in the legend from the menu or with the keyboard shortcut `Cmd + I`.

You can adjust settings for what cell info is shown in the hover settings:
![Menu_HoverSettings](/assets/documentation/Menu_HoverSettings.png)


### Selecting Hover Features 
Select which features will be shown in the legend when hovering over a cell:
![Hover_Legend_Settings](/assets/documentation/Hover_Legend_Settings.png)

You can select features manually:
![Hover_Legend_Feature_Selection](/assets/documentation/Hover_Legend_Feature_Selection.png)

We recommend to select the mean of the lineage features (Mean + Cell Types will be selected automatically) as well as any relevant subregions. See [Features Documentation](/documentation/features) for more info. 

You can also select a feature group (*Highly Recommended!*)
We create a `Lineage` feature group and select it here:
![Hover_Legend_Feature_Group](/assets/documentation/Hover_Legend_Feature_Group.png)

Compare the legend before filtering for only lineage markers:
![Select_Cell_Hover](/assets/documentation/Select_Cell_Hover.png){: width="90%"} 
and after filtering: 
![Select_Cell_Hover_Filter](/assets/documentation/Select_Cell_Hover_Filter.png){: width="90%"}  

In order for the hover info to be most informative to celltype identification, we filter out markers like DNA which are high for all cells. 


### Advanced Hover Legend Settings
In the advanced settings you can control: 
- Sorting Features
- Including Zero Values
- Limiting to Top #N Features
![Hover_Legend_Settings_Advanced](/assets/documentation/Hover_Legend_Settings_Advanced.png)

> We recommend sticking with the defaults (sorted & zero-excluded) for classification.

