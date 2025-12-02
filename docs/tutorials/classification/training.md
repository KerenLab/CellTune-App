---
layout: default
title: Training & Predictions
parent: Classification
grand_parent: Tutorials
nav_order: 3
permalink: /tutorials/classification/training
---

---

## Classifier Training and Predictions
&nbsp;  
Train the CellTune classifier using the features and labels.


### Train Classifier
&nbsp;  

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/Classification_Training.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>
&nbsp;  

- CellTune trains two models, XGBoost and CatBoost, by default. CatBoost is slow without GPU (1–2 hours), so LightGBM may be substituted if desired. Time can vary based on system. Please be patient.
- A backup copy of your labels is created each time you train. These are usually very small files.
- After training, you will see 4 new population sets Pred_ALL, Pred_MDL1, Pred_MDL2, and Pred_AVG. Pred_AVG, averages the probabilities of the two models to give one classification. Pred_ALL gives both classifications for each cell (it is one classification if they are the same classification). These 4 population sets will be updated each time you train.


--- 

### Visualize Predictions
&nbsp;  

You can select a population set and color the cells by the populations.  
Here we select the predictions from the classifier and visualize the predictions.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/VisualizePredictions.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

---

### Compare Predictions to Images of Protein Expression 
Here we make one population visible and make it transparent to compare it to the protein expression as shown:

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/VisualizePopulationsOpacity.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

---


### Import Prediction Probabilities
&nbsp;  

You can import the model's average probabilities and utilize them for review and gating.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/Classification_ImportProbabilities.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

Here we show gating by CD8T probability while verifying by looking at the image of CD8 expression. 
*Note this is an early model so it isn't expected to be great yet!*


---

