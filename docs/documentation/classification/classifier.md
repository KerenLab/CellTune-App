---
layout: default
title: Classifier
parent: Classification
grand_parent: Documentation
nav_order: 1
permalink: /documentation/classification/classifier
---

---

## Create a New CellTune Classifier
&nbsp; 

To create a classifier, click on the `+` button in the classification panel.

![Classification_Panel](/assets/documentation/Classification_Panel.png){: width="45%"}  

This will open a dialog the following dialog: 

![Classifier_Create](/assets/documentation/Classifier_Create.png){: width="75%"}  

1. You can fill in the classifier's name (Default = 'Classifier_1')
2. You need to select features that the classifier will use in training.

![Classification_Feature_Selection](/assets/documentation/Classification_Feature_Selection.png){: width="95%"}  

- It is recommended to select all features for the lineage markers. (We also select all features for any imported computed features).

![Feature_Selection_Regions](/assets/documentation/Feature_Selection_Regions.png){: width="95%"}  
- We only select `Cell Counts` features for Regions (Those two feature types are selected for you by default in the Region tab). Since these are binary masks, it is sufficient to know how much of the cell is in the mask. 


