---
layout: default
title: Classification Workflow
parent: Tutorials
nav_order: 5
permalink: /tutorials/classification-workflow
---

---

## Step 8: Classification

### 8A. Create Classifier
&nbsp;  

Create a classifier and select the features it will use for training.  
The features were computed or imported previously in Step 4.

<video width="100%" controls>
  <source src="{{ '/assets/tutorial/CreateClassifier.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

---

### 8B. Add Labels to Classifier
&nbsp;  

Add training labels to a classifier. You can select an existing population set.  
This action will create a new population set called `Labels_{Classifier_Name}`.

<video width="100%" controls>
  <source src="{{ '/assets/tutorial/ClassifierAddLabels.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

---

### 8C. Train Classifier
&nbsp;  

Train the CellTune classifier using the features and labels. Please be patient.

<video width="100%" controls>
  <source src="{{ '/assets/tutorial/ClassifierTraining.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

CellTune trains two models, XGBoost and CatBoost, by default. CatBoost is slow without GPU (1–2 hours), so LightGBM may be substituted if desired.

---

### 8D. Plot Confusions
&nbsp;  

Plot a confusion matrix showing the agreements and disagreements between the two models trained.

<video width="100%" controls>
  <source src="{{ '/assets/tutorial/PlotConfusions.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

