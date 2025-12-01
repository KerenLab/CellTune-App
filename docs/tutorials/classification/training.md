---
layout: default
title: Training & Predictions
parent: Classification
grand_parent: Tutorials
nav_order: 3
permalink: /tutorials/classification/training
---

---


## Train Classifier
&nbsp;  

Train the CellTune classifier using the features and labels. Please be patient.
&nbsp;   
&nbsp;  

<video width="100%" controls>
  <source src="{{ '/assets/tutorial/ClassifierTraining.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>
&nbsp;  

CellTune trains two models, XGBoost and CatBoost, by default. CatBoost is slow without GPU (1–2 hours), so LightGBM may be substituted if desired.



## Visualize Predictions
&nbsp;  

You can select a population set and color the cells by the populations.  
Here we select the predictions from the classifier and visualize the predictions.

<video width="100%" controls>
  <source src="{{ '/assets/tutorial/VisualizePredictions.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

You can put one population on and make it transparent to compare it to the protein expression as shown:

<video width="100%" controls>
  <source src="{{ '/assets/tutorial/VisualizePopulationsOpacity.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

---