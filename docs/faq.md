---
layout: home
nav_order: 5
title: FAQ
has_children: false
---

## Frequently Asked Questions
&nbsp;  

Q: ***What do I need to start? How should I prepare my data?***

A: *Before starting with CellTune, you’ll just need to organize your* ***multiplexed images*** *and* ***segmentations****. We highly recommend pre-processing your images to clean out background, noise, and artifacts. See [Data Preparation](/documentation/getting-started/data-preparation) for details on required formats, recommended structure, and pre-processing suggestions.*

*You can also **optionally** prepare a table of initial cell type information which can be used for automated landmarking and automated channel selection during cell review.*

&nbsp;  

Q: ***What segmentation tool do you recommend?***

A: *We've had positive experiences using [Instanseg](https://github.com/instanseg/instanseg), [Mesmer](https://deepcell.readthedocs.io/en/latest/app-gallery/mesmer.html), and [Cellpose](https://www.cellpose.org/).*

&nbsp;  

Q: ***I have an issue, bug report, request - how should I contact you?***

A: *You can reach us via GitHub Issues or email. For details, see our [Contact](/contact) page.*

&nbsp;  


Q: ***How should I label a cell that is ambiguous or has bad segmentation?***

A: *We prefer to skip these cells. You may alternatively label these cells as “Ambiguous”. CellTune will ignore them during training. We strongly prefer not to train on truly ambiguous cells. If you have a reasonable preference for a label, you can assign it to that — but avoid forcing a labeling into training when the signal is unclear.*

*We encourage following our lab's conventions:*
- *“Unidentified" = Cells that are negative for all lineage markers, lineage is unknown. [Unidentified comes up in every project and is always included in the training.]*
- *"Garbage" = Cells that are artifacts (e.g., multi-channel aggregates, overly positive for many markers, or otherwise unusable). [By default Garbage is included in training to find other similar cells, so it should be a recurring staining issue, otherwise filter out from training]*
- *"Ambiguous" or Skip = Cells that are ambiguous due to overlap or segmentation issues should be labeled “Ambiguous” or skipped entirely.*

*This keeps training data clean and ensures the classifier efficiently learns from high-quality examples.*

&nbsp;  


Q: ***How do I know when I should stop labeling?***

A: *So far all users found that labeling between ~100–200 cells per cell type was sufficient, regardless of dataset size. By that point, most newly sampled cells tend to be ambiguous, which is a good sign that the models have already learned the clear cases.*

*Agreement between the two internal models when plotting confusions can also serve as an indicator that you’re on the right track:*
- *\>85% for well-defined/stained cell types (e.g., CD8 T cells, B cells)*
- *\>90% for nuclear-marker-defined cell types (e.g., Tregs -> FoxP3⁺)*
- *\>65% for less well-defined categories (e.g., ImmuneOther, Unidentified)*
- *Balanced agreement between both models (percentages displayed on the right and bottom of the matrix should be similar to each other).*

*You can also inspect the full-image predictions and zoom into random regions to verify that the classifier behaves as expected. There is no strict stopping rule, since some datasets are inherently harder - often due to staining variability, weak markers, or challenging tissue contexts. The goal is simply to reach a point where the model produces accurate stable predictions.*


&nbsp;  

Q: ***Does CellTune work for spatial transcriptomics?***

A: *Not at the moment. CellTune is built for multiplexed protein imaging, and while many components could definitely extend to spatial transcriptomics, support is not available yet.*
