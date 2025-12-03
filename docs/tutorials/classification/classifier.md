---
layout: default
title: Classifier
parent: Classification
grand_parent: Tutorials
nav_order: 1
permalink: /tutorials/classification/classifier
---

---

## Create a Classifier
&nbsp;  

Create a new CellTune classifier and select the features it will use for training.  
The features were computed or imported [previously](/tutorials/features).
&nbsp;  

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/Classification_Create.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

- We usually select all features from **lineage** channels, as well as for any computed features (e.g. colocalization we have imported). We also include subregions we have, but only the `Cell` `Counts` features. (Since these masks are binary, we only care how much of the cell is in the mask.)

### Edit Classifier

You can change the features used in the classifier by selecting the classifier and clicking the edit button:

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/Classifier_EditFeatures.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

---