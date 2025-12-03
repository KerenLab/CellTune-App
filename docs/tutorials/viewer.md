---
layout: default
title: Viewer & Interface
parent: Tutorials
nav_order: 2
permalink: /tutorials/viewer
---

---

## Viewer & Interface 
&nbsp; 

---

### Viewer Basics: Select / Adjust Channels, Change Image, & Zoom
&nbsp;  

On the left side you have panels for the Images and Channels.
Select channels, either with the dropdown or by typing in the box.
Adjust channel brightness with the sliders.
The top left panel allows you to select different images from your project.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/ViewerBasicsChangeChannelImageZoom.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

> *Tip:* When an image is selected, you can scroll through images with the up and down arrows. You can also scroll through the channels by clicking (as if editing) and then scrolling up/down with the arrows!

---

### Create Channel Groups
&nbsp;  

Create channel groups (you can select and change groups of channels with a single click!):

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/ChannelGroups.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

Type the channel group name in the box, then press the (+) button.  
To delete a channel group press the (-) button.  
If you change the channels with an existing channel group name selected, the (+) button will update the channel group.  
> Tip: You can scroll through channel groups with the up and down arrows.


---

### Adjust Segmentation 
&nbsp;  

Adjust segmentation opacity and hover fill through segment controls.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/AdjustSegmentation.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>
<!-- AdjustSegmentationOpacity_2.mp4 -->

> Tip: 0.4 is our favorite opacity setting for the segmentation.

&nbsp;  

Show/Hide segmentation from `View` settings or with keyboard shortcut!
<video width="100%" controls>
  <source src="{{ '/assets/tutorials/ShowHideSegmentation.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

--- 

### Segment Controls & Select Cell
&nbsp;  

This video demonstrates how to adjust hover fill settings (the red highlight can switch from showing cell borders to filling the entire cell when hovering). 

Cells can be selected or unselected in the viewer by pressing `Shift` + `Left Click`. Selected cells are indicated by crosshairs. 

You can also select a cell by entering its ID in the segment controls, which will automatically zoom to that cell. The cell ID of the currently **hovered** cell (not selected cell) is displayed in the legend. 

*Note: Cell hover info shown in legend turned on with keyboard shortcut `Cmd` + `I`*

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/SelectCell.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>



---

### Colors and Color Blending
&nbsp;  

You can change the color of a channel with the colorbox to its left.  
  
When two channels overlap in the image, their colors blend.  
There are two different modes of color blending implemented in CellTune: 
 - `Additive` (Red + Yellow = Yellow)
 - `Paint Mix` (Red + Yellow = Orange)

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/ViewerBlendMode.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

---

### Segmentation Fill Borders Inclusion
&nbsp;  

When hovering over a cell (or when coloring cells by population or gate), CellTune highlights it either as a filled region or as borders only.
By default, the filled highlight does not include the cell borders. You can change this behavior in the Advanced Settings, as demonstrated in the video below.

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/ViewerAdvancedFilledBordersIncluded.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>


> Turning this setting off is recommended when working with [very large images](/tutorials/additional-tutorials/whole-slide-example). When zoomed out, most cells appear as “all borders,” so disabling border exclusion and using the filled view makes it easier to see cell colors consistently as you zoom in and out.


--- 

### Keyboard Shorcuts
&nbsp;

You can open a window that displays all available keyboard shortcuts and keep it visible while you work (especially useful if you have a second monitor).  

From the menu: `Help --> Keyboard Shortcuts`

<video width="100%" controls>
  <source src="{{ '/assets/tutorials/KeyboardShortcuts.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

----
