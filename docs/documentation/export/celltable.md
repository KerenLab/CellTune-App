---
layout: default
title: Export CellTable
parent: Export
grand_parent: Documentation
nav_order: 2
permalink: /documentation/export/celltable
---

---

## Export CellTable
&nbsp; 

You can export a CellTable that includes marker intensities, spatial features, and any subset of fields you choose. The exported table can also include population labels for each cell.  
CellTune supports `.csv`, `.parquet`, and `AnnData` outputs, making it easy to continue analysis in downstream environments such as Python, R, Scanpy, or Seurat.

1. Export the CellTable through Export → Cell Table.

    ![Menu_Export_CellTable](/assets/documentation/Menu_Export.png){: width="35%"}  

2. This will open the following dialog:

    ![Export_CellTable](/assets/documentation/Export_CellTable_Dialog.png){: width="75%"}
    
3. You can choose the output file type in the top drop down list:

    ![Export_CellTable_Options](/assets/documentation/Export_CellTable_Options.png){: width="45%"}  

4. In `Select Feature to Export` choose which feature are included in the exported table.

5. In `Select Population Sets to Include` you can choose to add population sets to the exported cell table. You can add multiple population sets.

6. The exported table will be saved in the project's `Tables` folder.

   


