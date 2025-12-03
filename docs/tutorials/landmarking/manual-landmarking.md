---
layout: default
title: Manual Landmarking
parent: Landmarking
grand_parent: Tutorials
nav_order: 1
permalink: /tutorials/landmarking/manual-landmarking
---

---
## Manual Landmark Gating 

### Manual Landmark Gating CD3+ T cells 
&nbsp;  

We start by creating a new empty population set for our landmarks. 

Here we gate for CD3+ T cells: CD3 high, CD4 low, CD8 low, & other non-T cell markers low like CD68 for example. 

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/LandmarkingManual_CD3T_1.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>


---

### Manual Landmark Gating CD4+ T cells 
&nbsp;  

As an example, we can adjust the CD3+ T gate with CD4 low to be CD4 high in order to gate for CD4+ T cells.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/LandmarkingManual_CD4T_2.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

> *Tip:* Don't forget that macrophages and other myeloid cells are often CD4+!  

---

### Manual Landmark Gating CD8+ T cells 
&nbsp;  

Similarly, we adjust the CD4 back to low and the CD8 to be high in order to gate for CD8+ T cells.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/LandmarkingManual_CD8T_3.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>


---

## Review Landmark Candidates
For each gate, we sampled candidates for review to be labeled as landmark cells.
We review each below.

### Review CD8+ T cells
*(The order you review them in doesn't matter. I happened to review them in the opposite order)*

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/LandmarkingManual_Review_CD8T_1.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

- *Important Note*, we are using the [keyboard shortcuts](/documentation/keyboard-shortcuts) (`Cmd` + `Right`) to go to the **Next Cell**.
- This way our cursor can be by the populations to click on the label very fast without moving the cursor.
- As you go to the **Next Cell**, the reviewed cell is automatically hovered on (when the cursor is not on the image)!

---

### Review CD4+ T cells

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/LandmarkingManual_Review_CD4T_2.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

---

### Review CD3+ T cells

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/LandmarkingManual_Review_CD3T_3.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

---


## More Challenging Example: `ImmuneOther`
In this example we are looking for CD45+ cells that are negative for other immune lineage markers. 

### Manual Landmark Gating ImmuneOther cells
&nbsp;  

We show a full example of adding many negative gates. 

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/LandmarkingManual_ImmuneOther_4_PostReview.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

*Note* we could add even more negative gates for other non-immune markers like SMA if we want to exclude those. But since we review the cells anyways it is ok. 

---

### Review ImmuneOther cells

Here we create the ImmuneOther class label for the first time.
ImmuneOther is defined by being negative for a lot of different channels, so we also create channel groups that will help us to review & label.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/LandmarkingManual_Review_ImmuneOther_4_CreateChannelGroup.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

Creating a channel group for non-immune proteins.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/LandmarkingManual_Review_ImmuneOther_4_CreateChannelGroup_2.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

Now we can use the [keyboard shortcuts](/documentation/keyboard-shortcuts) (`Cmd` + `Up/Down`) to very quickly cycle through channel groups. This helps greatly to check we didn't miss anything really fast. (We don't need to do these checks as much on cells that have very specific markers like CD8.)

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/LandmarkingManual_Review_ImmuneOther_4_CycleChannelGroup_3.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

---
