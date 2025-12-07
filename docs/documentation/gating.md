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

This documentation section introduces the `Gating panel` and explains its various functions, controls, and recommended workflows.

> *Also make sure to see our [gating tutorials](/tutorials/gating), which walk you through both basic and advanced gating techniques, showing how to use gating effectively as part of the broader CellTune workflow.*


### The Gating Panel
![Gating_Panel](/assets/documentation/Gating_Panel.png){: width="35%"}   


1. Select the data type.
(Currently, only cell-level gating is supported.)

2. Choose a feature to gate by.
	- Use the dropdown to select a feature.
	- You can also type directly into the box and press Enter to select a feature.
	- Click the filter icon to narrow the list so you aren’t overwhelmed by all spatial features.
	
		Before filtering:

		![Features_Filter_Gating_Dropdown_Full](/assets/documentation/Features_Filter_Gating_Dropdown_Full.png){: width="35%"} 
		
		After filtering:  

		![Features_Filter_Gating_Dropdown](/assets/documentation/Features_Filter_Gating_Dropdown.png){: width="35%"}   


3. View the histogram.
	- Once a feature is selected, a histogram appears. Adjust the gate by dragging the sliders or by clicking the threshold values and editing them directly. The gated cells update instantly.

4. Use the gated cells.
	When satisfied with your gate, you can:
	- `Apply Gate` to add additional gates on top of it.
	- `Create Population` from the gated cells.
	- `Sample & Review` cells from the gate for landmarking or verification.

**Buttons in the Gating Panel:**
- `Apply Gate`: Makes the current gate persistent and adds it to the gating expression; allows stacking multiple gates.
- `Remove Gate`: Removes the current gate.
- `View All Gates`: Opens a table showing all active gates and their thresholds.
![Gating_View_All_Gates](/assets/documentation/Gating_View_All_Gates.png){: width="55%"}
- `Clear All Gates`: Removes every applied gate.
- `Populations Filter`: Applies gating only to the currently selected populations.
- `Clear Populations`: Removes the population filter.
- `Create Population`: Creates a new population from the currently gated cells.
- `Sample & Review`: Samples all the cells from the current gate and creates a review from them. (You should use randomization - see [Review Documentation](/documentation/review))


### Gating Visibility & Opacity
At the top of the gating panel is a visibility icon, you can toggle on/off the gating. If it is on it will still be visible when the gating panel is minimized.  
You can adjust whether the gating color fills the selected cells or only shows their borders, as well as the gating opacity, from the `Segment Controls` panel. 


### Gating Histogram Plot Settings
<!-- To the right of the histogram there is a settings icon you can click on to edit the histogram settings: -->
To the right of the histogram there is a settings icon you can click on to edit the histogram settings <span style="vertical-align: middle;">![Toolbar_Label_Ambiguous](/assets/documentation/Toolbar_Review_Settings.png){: width="5%"}</span>:

![Gating_Plot_Settings](/assets/documentation/Gating_Plot_Settings.png){: width="45%"}
- Histogram Bins
- Min and Max of the range
- Whether to exclude zero values from the histogram (effectively min range 0.00001)



### Standard vs. Landmark Gating
When we typically think of gating, we are trying to set threshold to separate between positive and negative cells.
The following example shows a threshold we might apply on CD45 to separate CD45+ and CD45- cells.
[The cells highlighted in cyan would be gated as positive.]

![Gating_CD45_Regular](/assets/documentation/Gating_CD45_Regular.png){: width="100%"}   

> Notice where the threshold is on our histogram


For Landmark Gating, we only need to get a subset of highly confident positive cells. We want them to all be correct (not neighboring cells picking up spillover), therefore we set the gate very high, to only get highly expressing cells. 

![Gating_CD45_Landmarking](/assets/documentation/Gating_CD45_Landmarking.png){: width="100%"}   

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

![Gating_Edit_Expression_Before](/assets/documentation/Gating_Edit_Expression_Before.png){: width="65%"}

***BE CAREFUL WITH PARENTHESES!!!*** 
*You can delete parentheses if it makes it clearer for you to write.*

![Gating_Expression_Edit_After](/assets/documentation/Gating_Expression_Edit_After.png){: width="65%"}

After editing click `OK` and your expression will update:

![Gating_Expression_OR](/assets/documentation/Gating_Expression_OR.png){: width="35%"}


### Gating Populations Filter
Often we only want to gate a subset of a population.
We can filter by any population or several populations in the current population set.  

First, make sure you have exited `Review Mode` and no cell is selected (otherwise clicking on a population will label the cell).
Then, click on a population or several populations (multi-select/deselect with `Cmd`, select a range with `Shift`, select all with `Cmd + A`)

Click on the `Populations Filter` and you will see the populations being used underneath the gating expression:

![Gating_Population_Filter](/assets/documentation/Gating_Population_Filter.png){: width="40%"}


Only cells in the population will be gated by the features in the gating expression, as you can see here:

![Gating_PopulationFilter_FullView](/assets/documentation/Gating_PopulationFilter_FullView.png){: width="100%"}




