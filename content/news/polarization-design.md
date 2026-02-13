---
title: "Why rely on polarization-diversity with duplicated circuits, when you can program both polarizations into one?"
date: 2025-09-05
description: "Instead of duplicating circuits, we treat polarization as just another parameter to program directly into the geometry of our devices, just like we do for wavelength."
featureimage: "img/polarization-diversity.png"
showHero: true
related_publication_ids: ["vit2024towards", "vit2025polarization"]
---

Integrated photonics has always had a complicated relationship with polarization. The conventional solution has been **polarization-diversity schemes**: separate the two polarizations and route them through duplicate circuits—doubling both footprint and complexity.

We decided to flip the script. Instead of duplicating circuits, we treat polarization as just another parameter to **program directly into the geometry** of our devices, just like we do for wavelength.

<!--more-->

📄 Our recent article **“Universal on-chip polarization handling with deep photonic networks”** ([IEEE Journal of Lightwave Technology](https://ieeexplore.ieee.org/abstract/document/11080014)) shows how this paradigm shift enables a new class of versatile optical components.

### Rethinking Polarization
By cascading Mach–Zehnder interferometers with **polarization-aware phase delays**, we built a system where TE and TM modes are processed simultaneously—but differently. In this architecture, custom tapers provide independent phase control for each polarization, allowing the network to "learn" how to route light depending on its polarization state and wavelength.

### Programmable Functionality
Unlike conventional devices that just split or rotate, this system can be trained to implement arbitrary polarization transfer functions. It can:

*   **Balanced Splitting:** Split input evenly between two outputs, regardless of TE or TM polarization.
*   **Arbitrary Routing:** Route TE and TM light into different outputs, or distribute them across multiple channels.
*   **Wavelength Selectivity:** Combine polarization handling with wavelength selectivity (e.g., different behavior for C-band vs. L-band).
*   **High Performance:** Maintain performance across a 120 nm bandwidth with **>20 dB extinction** and **<0.5 dB excess loss**.

### The Architecture Revolution
The breakthrough lies in the **programmable phase-delay sections**. Instead of relying on fixed geometries, we construct custom taper profiles whose widths serve as learnable parameters. By optimizing for both polarizations simultaneously, the network converges to solutions in **under a minute**—achieving levels of functional freedom unattainable with traditional hand-designed structures.

### Why It Matters
This matters because polarization isn’t simply a constraint to manage—it’s an **information channel**. Concepts like polarization-multiplexed computing, programmable handling of quantum states, and multi-modal sensing become part of a unified design workflow that adapts seamlessly across applications.

Huge kudos to **Aycan Deniz Vit** (now at UGent Photonics Research Group) and the entire team for this outstanding effort! 👏

#PolarizationOptics #SiliconPhotonics #IntegratedOptics #PhotonicNetworks #OpticalEngineering
