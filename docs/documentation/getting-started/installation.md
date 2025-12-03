---
layout: default
title: Installation
parent: Getting Started
grand_parent: Documentation
nav_order: 2
permalink: /documentation/getting-started/installation
has_children: true
---

---

## Installation  

> Estimated installation time: 1-3 minutes  

### System Requirements  
&nbsp;  
**Operating Systems:**
- macOS 12 or later (Apple Silicon)
- Windows 10/11 (64-bit)

**Tested on:**
- macOS 12.6 (Intel), macOS 13.0 (M1), macOS 15.3 (M2)
- Windows 10 Enterprise (21H2), Windows Server 2019 Standard (1809)

**Dependencies:**
- All required dependencies are bundled inside the application. No additional installation is needed.
- Light mode only, dark mode support coming soon. 

**Hardware:**
- No special hardware required.
- ≥32 GB RAM and ≥8 CPU cores are highly recommended for efficient processing.
- A dedicated GPU (Apple Silicon or NVIDIA CUDA-capable) is highly recommended for improved performance, most especially for CNN-based features (e.g. marker positivity inference).
- Available hard disk memory approximately ~2X size of your project's compressed images (e.g. for 300GB of compressed OME-TIFFs, should free about 600GB of space, not including the OME-TIFFs themselves). 
- For best performance, it is currently recommended to work with data stored locally (we are working on testing and improving performance with remote disks). 

See the installation guides for [Mac](/documentation/getting-started/installation/macos) and [Windows](/documentation/getting-started/installation/windows).