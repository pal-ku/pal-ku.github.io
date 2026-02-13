---
title: "Accelerating Inverse Photonic Design with Factorization Caching"
date: 2023-08-12
description: "Our latest work introduces a multi-faceted factorization caching strategy that drastically reduces simulation runtimes in photonic inverse design."
featureimage: "img/factorization-caching.png"
heroStyle: "basic"
showHero: true
related_publication_ids: ["dasdemir2023computational"]
---

What if the bottleneck in inverse photonic design—solving Maxwell’s equations—could be scaled away?

Our latest work, published in **Applied Physics Letters**, introduces a multi-faceted factorization caching strategy that drastically reduces simulation runtimes in photonic inverse design. This approach enables up to **9.2× speedups** in device optimization, paving the way for efficient design of large-scale, multi-wavelength, and multi-mode nanophotonic devices.

### The Challenge in Inverse Design
Adjoint-based optimization has revolutionized the design of nanophotonic devices, enabling automated generation of compact, broadband components with remarkable performance. However, a critical limitation remains: the majority of computation time is spent on solving large sparse linear systems during forward and adjoint simulations.

Existing approaches such as Schur decomposition and deep learning alternatives either fail to generalize across device types or struggle with large device footprints.

### Our Solution: Factorization Caching
To address this challenge, we developed a caching framework that reuses both symbolic and numerical factorizations of the system matrix derived from the finite-difference frequency-domain (FDFD) method.

This framework capitalizes on three key observations:
1.  **Adjoint symmetry**: The adjoint system matrix is the transpose of the forward matrix, allowing reuse of the LU factors.
2.  **Fixed sparsity pattern**: Throughout optimization, the matrix structure (symbolic factorization) remains constant and can be reused.
3.  **Multi-input reuse**: The same cached factors can be applied to different input excitations during a given iteration.

### Results
We demonstrated this method on two inverse-designed silicon photonic components:
-   **Wavelength Duplexer**: Designed across 10 target wavelengths, reaching 4.7× speedup compared to the standard approach. Insertion losses were below 0.26 dB.
-   **Mode Multiplexer**: Supporting 3 input modes over a 100 nm bandwidth, this device achieved over 8.5× simulation acceleration.

These speedups remain effective across a wide range of device footprints—from 16 µm² up to 7000 µm²—without sacrificing physical accuracy.

### Why It Matters
Factorization caching bridges the gap between exact physics-based simulation and scalable, hardware-efficient optimization. Unlike deep learning-based surrogates, our method retains full accuracy while delivering near-order-of-magnitude runtime reductions. This makes large-scale and multi-functional device optimization practically feasible on standard CPU hardware.

### What’s Next?
We’re excited to extend this approach to:
-   3D and vectorial simulations using direct solvers
-   Fabrication-aware design workflows
-   Hardware acceleration (e.g., GPU-based back substitution)
-   General-purpose caching for other domains, including acoustics and electromagnetics
