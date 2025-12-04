---
layout: default
title: Interface
parent: Viewer & Interface
grand_parent: Documentation
nav_order: 1
permalink: /documentation/viewer/interface
---

---

## Viewer Interface
&nbsp; 

Once project setup completes, the main CellTune interface will load with your first image displayed:

![Viewer_0](/assets/documentation/Viewer_0.png)

Highlights:
- Left panel: select images and channels.
- Right panel: manage [populations](#populations-panel), [gating](#gating-panel), [classification](#classification-panel), and [segment controls](/documentation/viewer/segment-controls).
- Bottom [toolbars](/documentation/viewer/toolbars): labeling and review tools.
- Center: the image viewer, where selected channels are visualized overlayed with segmented cells. 

> You can zoom, pan, and select cells directly in the viewer. When hovering over cells, the cells are highlighted and dynamic [legends](/documentation/viewer/legends-hover) can display information and statistics in real time.

---

### Images Panel
&nbsp;  

The top left panel allows you to select different images from your project.
You can select images by scrolling through the list and clicking on an image name.
 
![Images_Panel](/assets/documentation/Images_Panel.png)

> Tip: When an image is selected, you can scroll through images with the up and down arrows.
  
&nbsp;
*We are planning to add an option to search in a future version.*


---

### Channels Panel

Below the images panel, you will find the channels panel with several channel widgets which allow you to select and adjust channels:

![ChannelWidget](/assets/documentation/ChannelWidget.png)

> *(By default there are 7, we are working on adding more)*

&nbsp;

**Adjust Brightness:**  
You can adjust channel brightness cutoffs using the sliders.
Everything below the left (bottom) slider handle will be black and everything above the right (upper) slider handle will be saturated.  
> Tip: You can click directly on the values and edit them (press Enter after typing!). You can also edit the value on the right side to increase/decrease the sliders range.


**Select Channel:**  
You can select channels using the dropdown or by typing in a channel name (***make sure you press Enter!***)
 
![Channels_Select_Dropdown](/assets/documentation/Channels_Select_Dropdown.png)

You can also use the *Up/Down Arrows* to change channels when you click inside the channel text box (as if you are going to type).

> *Note you won't see a channel in the dropdown if it is already selected for a different channel widget.*


**Channel Color:**  
You can change the color of channels using the color selection box by clicking on one of the predefined colors, or using the hex or RGB inputs at the bottom:

![Channels_Color](/assets/documentation/Channels_Color.png)

**Visibility:**  
Each channel has an eye icon which can toggle its visibility.
At the top of the panel is an eye icon which toggles the visibility of all channels.

![ChannelGroups](/assets/documentation/ChannelGroups.png)

There is also a section at the top to select and save/delete channel groups, as discussed in the following section:

---

### Create Channel Groups
&nbsp;  

Create channel groups (you can select and change groups of channels with a single click!):



Type the channel group name in the box, then press the (+) button.  
To delete a channel group press the (-) button.  
If you change the channels with an existing channel group name selected, the (+) button will update the channel group.  
> Tip: You can scroll through channel groups with the up and down arrows.

---


### Channel Groups

Channel groups allow you to store and toggle sets of 7 channels at once. **DO NOT SKIP! They are extremely useful** for efficient visualization, review, and labeling. 
There are several [tutorials with examples](/tutorials/landmarking/clustering-landmarking#review-sample-for-landmarking) using them.  
*Anyone not using channel groups is missing out on the full CellTune experience—and for that, we shed a small, pixelated tear.*

  
**Creating a Channel Group:**
1. Select the channels desired in the channel widgets.
2. Type the name in the box.
3. Click on the `+` button next to the name to save. 

**Deleting a Channel Group:**
- Click on the `-` button on the right of the selected channel group.


For example, we usually start by saving an `Overview` channel group which includes CD45, SMA, CD31, ECAD/Keratin, and 2-3 others depending on the tissue in order to differentiate between the major cell type groups (Immune, Stroma, Vasculature, Epithelial, Tumor, etc.).

![Channel_Group_Overview](/assets/documentation/Channel_Group_Overview.png)

When the channel group is created you will see the following:

![Channel_Group_Created_Done](/assets/documentation/Channel_Group_Created_Done.png)

We also make a general `Immune` channel group, including CD20, CD3, CD68, CD15, IgA, etc to differentiate between the major immune groups (B cell, T cell, Macrophage, Neutrophil, Plasma, etc.):

![Channel_Group_Immune](/assets/documentation/Channel_Group_Immune.png)

We also make groups for `Tcell` (CD8, CD4, FOXP3), `Myeloid` (CD14, CD68, CD163, CD206, Calprotectin), and more

You can select a channel group using the dropdown, or more efficiently using the keyboard shortcut `Cmd + Up/Down` (mac).

![Channel_Group_Select](/assets/documentation/Channel_Group_Select.png)


--- 

### Populations Panel


Populations_Panel.png



---

### Gating Panel

Gating_Panel.png


---

### Classification Panel


Classification_panel.png


---

### Advanced Viewer Settings

You can adjust color blending and segmentation fill settings from the menu:

![Menu_AdvancedViewerSettings](/assets/documentation/Menu_AdvancedViewerSettings.png)


![Viewer_AdvancedSettingsDialog](/assets/documentation/Viewer_AdvancedSettingsDialog.png)

Color blending determines how two overlapping colors will appear when they mix. [See the tutorial for an example](/tutorials/viewer#colors-and-color-blending).

Segmentation fill settings determine whether or not the cell borders are included when highlighting a cell. [See the tutorial for an example](/tutorials/viewer#segmentation-fill-borders-inclusion).



---

Next see [Legends & Hovering](/documentation/viewer/legends-hover), [Segment Controls](/documentation/viewer/segment-controls), or [Toolbars](/documentation/viewer/toolbars).

---
