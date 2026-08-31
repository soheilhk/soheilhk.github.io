---
title: "Effective Apodization in Synthetic Aperture Ultrasound Computed Tomography"
publications:
  - Conf_IEEE_IUS2024_Hakakzadeh_et_al_Apo
collection: research
category: usct
date: 2025-09-01
venue: "Ring-Array / Beamforming"
excerpt: "A novel receive apodization framework for large-aperture SA-RUCT that mitigates diffraction, phase distortion, and grating lobes—delivering up to ~60% spatial resolution improvement and superior PSNR in phantom and in-vivo reconstructions."
image: "images/research/usct/ruct11.PNG"
image_caption: "Comparison of experimental and in-vivo imaging results using the 
conventional method and the proposed apodization technique. (a1, a2) 
Experimental images show artifact suppression and improved feature 
clarity with the proposed method. (b1, b2) In-vivo images demonstrate 
enhanced resolution and contrast, particularly in tissue boundaries and 
internal structures, when using the proposed technique. Yellow and red 
arrows highlight areas of significant improvement. "
expanded: true
---

### Overview & Motivation
Synthetic aperture reflection ultrasound computed tomography (SA-RUCT) provides comprehensive full-view acoustic reflectivity maps by synthesizing large receiving apertures from multi-angle transmits. However, scaling up the active receive aperture (large number of receiving elements, $R_x$) introduces severe acoustic degradation:
- **Phase Aberration & Wavefront Distortion:** Off-axis acoustic paths traverse heterogeneous speed-of-sound boundaries at steep incidence angles, leading to destructive interference during coherent summation.
- **Diffraction & Grating Clutter:** Unweighted or sub-optimally apodized wide receive apertures amplify acoustic diffraction artifacts and side-lobe leakage, deteriorating the Peak Signal-to-Noise Ratio (PSNR) and masking low-contrast microstructures.

This project presents an **optimized, dynamic apodization scheme** specifically tailored to SA-RUCT geometries that selectively suppresses corrupted high-angle receive contributions while maximizing coherent signal integration across the focal synthesized aperture.

---

### Key Technical Details & Methodology

- **Diffraction- & Distortion-Aware Weighting Function:**
  - Formulates an adaptive spatial/angular apodization profile across the synthesized receiver aperture:
    $$w(r, \theta_{Rx}) = f\big(\angle(\mathbf{k}_{inc}, \mathbf{k}_{scat}), \text{Directivity}(Rx)\big)$$
  - Dynamically downweights receive paths subject to excessive phase distortion and acoustic diffraction at wide angular deviations, mitigating off-axis incoherent clutter.
- **Coherent Synthetic Aperture Compounding Enhancement:**
  - Preserves full central acoustic wave coherence during delay-and-sum / synthetic aperture back-projection, preventing destructive phase cancellation at targeted focal points.
- **Multi-Platform Validation Pipeline:**
  - Benchmarked across full numerical wave-propagation simulations ($k$-Wave), multi-element ring-array phantoms, and *in-vivo* preclinical datasets.

---

### Quantitative Performance & Key Findings

| Metric / Feature | Conventional SA-RUCT Apodization | Proposed Optimized Apodization |
| :--- | :---: | :---: |
| **Spatial Resolution Enhancement** | Baseline | **Up to ~60% Improvement** |
| **Artifact & Clutter Suppression** | High (diffraction & side-lobe streaks) | **Near-Complete Suppression** |
| **Peak Signal-to-Noise Ratio (PSNR)** | Degraded at wide $R_x$ apertures | **Substantially Boosted across full ROI** |
| **Fine Structural Delineation** | Blurred boundaries & low contrast | **Sharp, isotropic edge delineation** |

---

### In-Vivo & Clinical Implications
- **Artifact-Free Preclinical & Clinical Breast Imaging:** Resolves micro-calcifications and subtle acoustic boundaries by preventing the clutter buildup typical of wide-angle circular transducer arrays.
- **Plug-and-Play Integration:** Seamlessly integrates into existing GPU/CPU beamforming pipelines without requiring iterative optimization or complex inversion loops, maintaining high frame-rate reconstruction capabilities.
