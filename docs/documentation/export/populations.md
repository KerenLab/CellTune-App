---
layout: default
title: Export Populations
parent: Export
grand_parent: Documentation
nav_order: 1
permalink: /documentation/export/populations
---

---

## Export Populations 
&nbsp; 

1. Select the population set you want to export in the population panel.

    ![Classification_Predictions_PopulationSets](/assets/documentation/Classification_Predictions_PopulationSets.png){: width="35%"}  

2. Export the population set through Export → Populations.

    ![Menu_Export_Populations](/assets/documentation/Menu_Export_Populations.png){: width="35%"}  

CellTune will save both:
- the population set file ('.csv' or '.parquet'), and
- a corresponding .info file containing the population set metadata (equivalent to a CellTypeTable).

Both files are written to the same folder using the name you selected.
![PopulationsInfo_File](/assets/documentation/Import_PopulationsInfo_File.png){: width="95%"}  


When completed successfully you should see the following:
![Export_Populations_Done](/assets/documentation/Export_Populations_Done.png){: width="85%"}  


These exported population sets and info can be easily used in downstream analyses, edited, and/or shared with collaborators.
