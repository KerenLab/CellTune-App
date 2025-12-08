---
layout: default
title: Add Labels
parent: Classification
grand_parent: Documentation
nav_order: 2
permalink: /documentation/classification/add-labels
---

---

## Add Labels to a Classifier
&nbsp; 

Once you have created a classifier, you need to add labels to it. 

1. In the classification pane, select your classifier from the list and click on `Add Labels`.

    This will open the following dialog:

    ![Classification_Add_Labels](/assets/documentation/Classification_Add_Labels.png){: width="75%"}  

    - The selected labels will be added as a new population set. You can edit the labels population name (Default = 'Labels_{CLASSIFIER_NAME}')
2. In `Label Import Option`: By default, if it's the first time adding labels to the classifier, select `Replace existing labels`.
3. In `Select Labels Source` you can choose between using labels `From existing population set`, or `Import population set` from a path.
    For example, for the first labeling round you will select the landmarks as the classifier labels.
    - Click on `Filter Populations` if you don't want to use all populations from the selected or imported population set.
4. If your classifier already has labels and want to modify them, select `Replace existing labels` in `Label Import Options`. This will open the `Existing label policy` section:
    - `Replace with new`: If a cell from the new labels file exists in the current labels, replace its label with that of the new file.
    - `Keep old labels`: If a cell from the new labels file exists in the current labels, keep its current label.
    - `Keep both labels`: If a cell from the new labels file exists in the current labels, add the new label. In this case the cell will have 2 labels.

    ![Classification_Add_Labels](/assets/documentation/Classification_Add_Labels_to_existing.png){: width="75%"}  

5. Click `OK` to add the labels to the classifier.