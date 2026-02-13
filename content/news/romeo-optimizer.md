---
title: "Rapid Optical Eigenmode Optimizer: Rethinking Photonic Simulation"
date: 2024-11-22
description: "With our recently published design framework ROMEO, we’re beginning to see what’s possible when simulation times are reduced from hours to milliseconds."
featureimage: "img/romeo.png"
showHero: true
related_publication_ids: ["oktay2024computationally"]
---

What if you could simulate a photonic device in **milliseconds** instead of minutes or hours?

This is no longer just an idea. With our recently published design framework **ROMEO** (Rapid Optical Eigenmode Optimizer), we’re beginning to see what’s possible when simulation times are drastically reduced.

As photonics continues to expand into new applications, there’s growing demand for ultra-efficient, compact, and broadband photonic devices. Algorithmically optimized (or inverse-designed) structures offer a promising approach, but the physical simulations required often dominate the computational cost. To make meaningful progress, we need much faster (and still accurate) simulation techniques. That’s where **ROMEO** comes in.

<!--more-->

### The Path to ROMEO
Modern AI-driven software tools can revolutionize physical simulation algorithms, enabling faster and more effective device optimization. The **Eigenmode Expansion (EME)** method, despite its potential for leveraging modern matrix algebra and parallel processing, has remained largely untapped for this purpose—until now.

*   **The Problem:** While GPUs are lightning-fast at scattering matrix operations, calculating scattering elements in EME is traditionally too slow for iterative optimization workflows.
*   **The Solution:** To tackle this, former student **Mehmet Can Oktay** (now at Ghent/imec) built a database of pre-computed scattering elements. This allows us to represent light scattering in arbitrary continuous geometries, like tapers, by cascading scattering matrices in parallel using PyTorch on a GPU.

### Unprecedented Speed and Accuracy
Using this framework, we demonstrated the ability to simulate arbitrary tapers in just **40 milliseconds**. 

In our recent publication in the *Journal of Lightwave Technology*, we showed ROMEO’s application to designing photonic components—including tapers, splitters, and crossings—in just **seconds**. 

*    **Performance:** Losses below 0.1 dB
*    **Bandwidth:** Ultra-wideband operation (exceeding 100-200 nm)
*    **Verification:** Confirmed by 3D-FDTD simulations and recent SiEPIC tapeouts.

Special thanks to the **SiEPIC openEBL team** for making the experimental verification possible!

### What’s Next?
ROMEO is just the beginning. We are looking to explore:
*   **Fabrication tolerance:** Directly integrating lithography models (e-beam or DUV) into the optimization.
*   **Ultra-broadband designs:** Optimizing performance over even wider wavelength ranges.
*   **New geometries:** Extending ROMEO beyond continuous waveguide structures to free-form inverse designs.
*   **Active devices:** Employing data-driven EME for optimizing modulator and detector geometries.

#SiliconPhotonics #IntegratedOptics #EME #SimulationSpeed #PhotonicDesign #InverseDesign #ROMEO
