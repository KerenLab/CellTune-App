---
layout: default
title: CellType Table
parent: Data Preparation
grand_parent: Getting Started
nav_order: 4
permalink: /documentation/getting-started/data-preparation/celltype-table
has_children: false
---

---

## CellType Table
`CellTypeTable.csv`  
Location: *`CellTune_Store/CellTune_Data/{PROJ_NAME}/Tables/`*  
[Example Below](#example-celltypetablecsv)  

---

### Cell Type Names
Column name: `CellType` (or `class`)
Description: 

---


### Primary Marker Column
Column name: `PrimaryMarker`
Description:

---

### Secondary & Tertiary Marker Columns
Column names: `SecondaryMarker` and `TertiaryMarker`
Description:

---

### Associated Channel Columns
Column names: `Channel_1`, `Channel_2`, `Channel_3`
Description:

---

### Color Column
Column name: `hex`
Description:

### **Cell Type Colors!**
As you can see, we feel very strongly about celltype colors.
We spent a lot of time generated a color palette of over 30 colors we can differentiate easily between.
Then made a default assignment for the major cell types.

**CellTune CytoPalette**


We use this as a starting point for our projects, and then make minimal adjustments to it - adding the cell types that aren't present and swapping some assignments if there is something specific we want to contrast even more. e.g. if our project was specifically about Neutrophils in the Tumor we might want to make them further apart, instead of Blue and Purple we might move the Neutrophils to be Pink or Orange. 

---

### Example CellTypeTable.csv


> Example table can be downloaded from the [demo data](#/tutorials/getting-started/demo-data) of the tutorials.

--- 