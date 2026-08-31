---
title: "Advanced Signal Restoration & Reconstruction for Limited-View and Bandwidth-Constrained PAI"
publications:
  - Conf_IEEE_IUS2022_Hakakzadeh_et_al_Unipolar
  - Paper_Journal_OPTICA_BOE2023_Hakakzadeh_et_al_Signal
  - Conf_IEEE_ICBME2022_Hakakzadeh_et_al_Hilbert
collection: research
category: pat
date: 2023-01-01
venue: "Linear-Array / Bandwidth and Axial Resoloution Improvement"
excerpt: "Advanced signal restoration and beamforming for limited-view and bandwidth-limited PAI, delivering near full-view fidelity, 50% resolution enhancement, and up to 80% background artifact reduction."
image: "images/research/pat/pat6.PNG"
image_caption: "Figure 1:    The experimental results of the right forearm of a 30-years old human hand. (a) a
photograph of the right forearm. The purple dashed line indicates the location of the imaging
region cross-section. (b) the dominant map of a human hand’s arteries and nerves; UN,
ulnar nerve, UA, ulnar artery; RA, radial artery. The blue rectangle indicate the position
of the linear array probe. (c, d) are the results of DAS and DMAS based on the initial PA
signal, respectively. (e, f) are the results of DAS and DMAS based on restored PA signal,
respectively."
expanded: true
---

**Key Technical Details & Innovations:**
- **Unipolar Back-Projection (Limited-View Compensation):** Formulates a unipolar reconstruction framework leveraging raw PA signals alongside their temporal derivatives. This resolves bipolar acoustic cancellation and enables half-view ($180^\circ$) circular apertures to reach near full-view ($360^\circ$) reconstructed image fidelity ($\text{gCNR} = 0.96$).
- **Hilbert-Based Coherence Factor (H-CF):** Solves the classic "data loss" (over-suppression) failure mode of standard coherence factors in planar PAI geometries by combining envelope information via the Hilbert transform with adaptive phase-coherence weighting.
- **Pre-Reconstruction Signal Restoration Mask:** Introduces an acoustic mask pipeline designed to eliminate axial ringing and transducer bandwidth-limitation ripples prior to beamforming (DAS/DMAS), significantly suppressing sidelobes along the acoustic propagation axis.
- **Multi-Modal Validation:** Benchmarked across numerical point/phantom targets, physical tungsten wire targets, and *in-vivo* human forearm imaging datasets.
- **Quantitative Performance Benchmarks:**
  - **Resolution Enhancement:** Achieves a **$\sim 50\%$ improvement** in limited-view spatial resolution and a **$45\%$ gain** in axial resolution for bandwidth-limited transducers.
  - **Contrast & Visibility:** Boosts Contrast Ratio ($\text{CR}$) by **$16.1\text{ dB}$** and elevates $\text{gCNR}$ by **$\sim 50\%$**.
  - **Artifact Suppression:** Delivers up to an **$80\%$ reduction** in background clutter and out-of-focus sidelobe artifacts.
