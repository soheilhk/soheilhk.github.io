---
title: "Quantitative Speed-of-Sound & Attenuation Tomography via FWI"
collection: research
category: usct
date: 2024-11-15
venue: "Medical Physics / Computational Imaging"
excerpt: "GPU-accelerated adjoint-state Full Waveform Inversion (FWI) for quantitative acoustic parameter mapping in transmission USCT."
image: "/images/research/usct-fwi.jpg"
image_caption: "Figure 2: Reconstructed sound speed map showing sub-millimeter lesion boundary differentiation."
paperurl: "https://doi.org/10.1002/your-fwi-paper"
codeurl: ""
slidesurl: ""
---

**Key Technical Details & Innovations:**
- **Adjoint-State Wavefield Modeling:** Time-domain acoustic wave equation propagation solved on CUDA cores with PML boundary conditions.
- **Cycle-Skipping Mitigation:** Multi-scale frequency continuation combined with envelope inversion to secure global convergence.
- **Quantitative Tissue Characterization:** High-contrast spatial resolution for identifying malignant vs. benign tissue via calibrated SOS/attenuation distributions.
