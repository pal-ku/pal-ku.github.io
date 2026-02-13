---
title: "Why rely on polarization-diversity with duplicated circuits, when you can program both polarizations into one?"
date: 2025-09-05
description: "Instead of duplicating circuits, we treat polarization as just another parameter to program directly into the geometry of our devices, just like we do for wavelength."
featureimage: "img/polarization-diversity.png"
showHero: true
related_publication_ids: ["vit2024towards", "vit2025polarization"]
---

Integrated photonics has always had a complicated relationship with polarization. On one hand, high-index contrast in the silicon-on-insulator platform gives us incredible compactness and functionality. On the other hand, those same properties also make devices respond very differently to TE and TM modes. The conventional solution is polarization-diversity schemes: separate the two polarizations, route them through duplicate circuits (doubling footprint and complexity), and then recombine or rotate them back together. These workarounds get the job done, but at the cost of scalability, adaptability, and design effort.

We decided to flip the script. Instead of duplicating circuits, we treat polarization as just another parameter to program directly into the geometry of our devices, just like we do for wavelength. This shift is at the heart of our universal photonic design framework, where computational optimization and programmable architectures open new frontiers for on-chip optical networks.

<!--more-->

📄 Our recent article **“Universal on-chip polarization handling with deep photonic networks”** ([IEEE Journal of Lightwave Technology](https://ieeexplore.ieee.org/abstract/document/11080014)) shows how this works. 

🔍 **The Insight: Polarization as Information**

Our former student **Aycan Deniz Vit** (now at UGent Photonics Research Group) led this breakthrough. By cascading Mach–Zehnder interferometers with polarization-aware phase delays, he built a system where TE and TM modes are processed simultaneously—but differently. In this architecture, custom tapers provide independent phase control for each polarization, allowing the network to learn how to route light depending on its polarization state (and also wavelength).

Unlike conventional devices that just split or rotate, this system can be trained to implement arbitrary polarization transfer functions. For example, it can:

*   Split optical input evenly between two outputs, regardless TE or TM polarization
*   Route TE and TM light into different outputs, or distribute TM light arbitrarily across multiple channels
*   Combine polarization handling with wavelength selectivity, enabling different behavior for C-band vs. L-band inputs
*   Maintain performance across a 120 nm bandwidth with >20 dB extinction and <0.5 dB excess loss

In other words, it’s no longer about building “a polarization splitter” or “a rotator.” It’s about programming the behavior you want.

⚙️ **The Architecture Revolution**

The breakthrough lies in the phase-delay sections. Instead of relying on fixed geometries, we construct custom taper profiles whose widths serve as learnable parameters. By optimizing for both polarizations simultaneously, the network converges to solutions in under a minute—achieving levels of performance and functional freedom unattainable with traditional hand-designed structures. In effect, it’s teaching silicon to recognize and manipulate polarization.

This matters because polarization isn’t simply a constraint to manage—it’s an information channel. With this approach, arbitrary polarization behavior can be programmed into a single architecture, instead of duplicating circuits or designing new components for each task. As a result, concepts like polarization-multiplexed computing, programmable handling of quantum states, and multi-modal sensing that fuses spectral and polarization information become part of a unified design workflow that can adapt seamlessly across applications.

👏 Huge kudos to Aycan and everyone who contributed — an outstanding effort that made this work possible! We’re proud of the team behind this achievement and the creativity and dedication they brought.

#PolarizationOptics #SiliconPhotonics #IntegratedOptics #PhotonicNetworks #OpticalEngineering
