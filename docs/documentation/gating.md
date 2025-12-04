---
layout: default
title: Gating
parent: Documentation
nav_order: 8
permalink: /documentation/gating
---

---
## Gating 

Gating is a powerful way to explore and separate cell populations, but spillover and overlapping markers make it difficult to classify all cells accurately using gates alone. CellTune enhances this process with tools for cell sampling, review, landmark gating, and complex gate construction, allowing you to iteratively refine populations and build high-quality cell type definitions.

This documentation section introduces the Gating panel and explains its various functions, controls, and recommended workflows.

> *Also make sure to see our [gating tutorials](/tutorials/gating), which walk you through both basic and advanced gating techniques, showing how to use gating effectively as part of the broader CellTune workflow.*


### The Gating Panel
![Gating_Panel](/assets/documentation/Gating_Panel.png){: width="35%"}   

1. First, you select the data type (*Currently only Cell gating is supported.*)

2. Then you select the feature you want to gate by.
- To the right of the feature dropdown is a filter button so you can filter down the features and not be overwhelmed by scrolling through all the spatial features calculated.
- You can also type in the box to select a feature (press Enter when done typing).

3. Un
### Gating Histogram Plot Settings
![Gating_Plot_Settings](/assets/documentation/Gating_Plot_Settings.png){: width="35%"}
- Histogram Bins
- Min and Max of the range
- Whether to exclude zero values from the histogram (effectively min range 0.00001)


You can view all the gates you have set at any time by clicking `View All Gates`:
![Gating_View_All_Gates](/assets/documentation/Gating_View_All_Gates.png){: width="35%"}



### Standard vs. Landmark Gating
When we typically think of gating, we are trying to set threshold to separate between positive and negative cells.
The following example shows a threshold we might apply on CD45 to separate CD45+ and CD45- cells.
[The cells highlighted in cyan would be gated as positive.]

![Gating_CD45_Regular](/assets/documentation/Gating_CD45_Regular.png){: width="35%"}   

> Notice where the threshold is on our histogram


For Landmark Gating, we only need to get a subset of highly confident positive cells. We want them to all be correct (not neighboring cells picking up spillover), therefore we set the gate very high, to only get highly expressing cells. 

![Gating_CD45_Landmarking](/assets/documentation/Gating_CD45_Landmarking.png){: width="35%"}   

> Notice where the threshold is now on our histogram 

This concept is critical for understanding how we manually and automatically perform landmark gating.


### Setting Multiple Consecutive Gates
As we apply additional gates, we can see that they are added to our gating expression at the bottom of the panel.
![Gating_CurrentExpression](/assets/documentation/Gating_CurrentExpression.png){: width="35%"}
... 
![Gating_Expression_2](/assets/documentation/Gating_Expression_2.png){: width="35%"}
...
![Gating_Expression_3](/assets/documentation/Gating_Expression_3.png){: width="35%"}

> The colors are meaningless

Already applied gates should appear bold in the gating feature dropdown:

![Gating_Bold_Feature_Dropdown](/assets/documentation/Gating_Bold_Feature_Dropdown.png){: width="35%"}   


### Edit Gating Expression
By default the gating expression uses all AND (&) operators. We can edit it to use OR (|) and NOT(!) 
> [*NOT is less commonly used - you can just equivalently set the threshold to be low if it was high before.*]

Click on the edit icon next to the expression.
![Gating_Expression_4](/assets/documentation/Gating_Expression_4.png){: width="35%"}

This will open a dialog where you can edit the current gating expression:
![Gating_Edit_Expression_Before](/assets/documentation/Gating_Edit_Expression_Before.png){: width="35%"}

***BE CAREFUL WITH PARENTHESES!!!*** 
*You can delete parentheses if it makes it clearer for you to write.*

![Gating_Expression_Edit_After](/assets/documentation/Gating_Expression_Edit_After.png){: width="35%"}

After editing Click `OK` and your expression will update:

![Gating_Expression_OR](/assets/documentation/Gating_Expression_OR.png){: width="35%"}


### Gating Populations Filter
Often we only want to gate a subset of a population.
We can filter by any population or several populations in the current population set.  

First, make sure you have exited Review Mode and no cell is selected (otherwise clicking on a population will label the cell).
Then, click on a population or several populations (multi-select/deselect with `Cmd`, select a range with `Shift`, select all with `Cmd + A`)

Click on the `Populations Filter` and you will see the populations being used underneath the gating expression:

![Gating_Population_Filter](/assets/documentation/Gating_Population_Filter.png){: width="40%"}


Only cells in the population will be gated by the features in the gating expression, as you can see here:

![Gating_PopulationFilter_FullView](/assets/documentation/Gating_PopulationFilter_FullView.png){: width="100%"}




