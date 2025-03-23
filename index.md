<style>
#splash-screen {
	position: fixed;
	top: 0;
	left: 0;
	width: 100vw;
	height: 100vh;
	background: white;
	display: flex;
	justify-content: center;
	align-items: center;
	z-index: 9999;
	transition: opacity 0.5s ease;
}
#splash-screen img {
	max-width: 200px;
}
</style>

<div id="splash-screen">
	<img src="/assets/celltune_logo.svg" alt="CellTune Logo">
</div>

<script>
window.addEventListener('load', () => {
	const splash = document.getElementById('splash-screen');
	splash.style.opacity = 0;
	setTimeout(() => {
		splash.style.display = 'none';
	}, 500); // Matches the CSS transition
});
</script>

---
layout: home
nav_order: 1
title: Introduction
---

# Welcome to CellTune
&nbsp;  
**CellTune is an integrative software to expedite accurate cell classification in spatial proteomics**. 

Designed for researchers analyzing large cohorts of spatial proteomics data, CellTune streamlines cell classification through a comprehensive and highly optimized human-in-the-loop active learning workflow. By strategically selecting cells with high uncertainty, the platform maximizes the impact of user input and enables the discovery of fine-grained and novel cell types. CellTune advances core capabilities across visualization, gating, annotation, and spatial feature extraction — all within a unified, intuitive, and code-free interface — to efficiently achieve state-of-the-art classification accuracy and resolution at scale.

To benchmark CellTune, we created [***CellTuneDepot***](#celltunedepot)—the largest fully manually labeled multiplexed imaging dataset to date—comprising over 40,000 cells comprehensively annotated by experts across 30 cell types. In addition, CellTuneDepot contains over 3 million high-quality semi-supervised labels generated with CellTune across a variety of tissues and disease states with accuracy comparable to expert annotation.

Together, CellTune and CellTuneDepot provide a powerful toolkit for classifying cells and accelerating biological discovery in spatial proteomics.


---
## Getting Started
>[Download & Install](#download.md)  
>[Documentation](#documentation)  
>[Tutorials](#tutorials)  
>[CellTuneDepot](#celltunedepot)  
>[Manuscript](#citation)  

---
© {{ site.time | date: '%Y' }} Weizmann Institute of Science. All rights reserved.
