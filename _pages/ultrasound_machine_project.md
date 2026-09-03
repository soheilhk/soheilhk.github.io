---
title: "End-to-End Clinical Ultrasound & Echocardiography Machine"
permalink: /ultrasound_machine_project/
author_profile: true
---

This project encompasses the full-stack design, development, and clinical translation of next-generation clinical ultrasound platforms—ranging from mid-range cart systems (**Luna**, **Zino**) and high-end platforms (**Hirman**) to compact handheld devices. 

The architecture bridges custom analog/digital front-end hardware (AFE, FPGA), real-time GPU beamforming pipelines (CUDA/C++), and an intuitive dual-screen clinical user interface (Qt/QML).

---

## 1. System Architecture & Hardware-Software Pipeline

The platform follows a modular, low-latency architecture optimized for high frame rates, adaptive acoustic beamforming, and responsive clinical control.

![Ultrasound System Architecture](../images/projects/ultrasound/ControlUnit.PNG)
*Figure 1: End-to-end hardware and processing architecture linking Front-End Beamformer, FPGA/AFE modules, Host processing unit, GPU compute engine, and clinical I/O consoles.*

### Core Architectural Subsystems
*   **Analog Front-End (AFE) & High-Voltage Pulser/Switches:** Multi-channel transmit/receive circuitry driving diverse probe topologies (Phased/Sector, Linear, Convex, Intraractal).
*   **FPGA Acquisition Hub:** High-speed serialized RF data capture, digital demodulation, decimation, and PCIe/USB data streaming to the host system.
*   **GPU Compute Pipeline (CUDA / C++):** Real-time software beamforming, analytical signal processing, scan conversion, and dynamic filter execution directly on GPU memory.
*   **Host Subsystem & I/O:** Dual-display driving architecture managing the high-refresh primary clinical monitor, secondary multi-touch screen, and physical control console.

---

## 2. Advanced Beamforming & Real-Time Signal Processing

To achieve high contrast resolution and edge preservation across deep and superficial imaging depths, advanced beamforming schemes were designed, simulated, and deployed in CUDA/C++:

*   **Adaptive Beamformers:**
    *   **Delay-and-Sum (DAS):** Base low-power, high-frame-rate standard beamforming.
    *   **Minimum Variance (MV):** Data-dependent adaptive weight calculation for side-lobe suppression and lateral resolution sharpening.
    *   **Delay-Multiply-and-Sum (DMAS):** Non-linear spatial correlation beamforming for enhanced speckle SNR and cyst contrast.
    *   **Short-Lag Spatial Coherence (SLSC):** Coherence-based imaging minimizing clutter and acoustic reverberation artifacts.
*   **Real-Time Post-Processing & Filtering:**
    *   Dynamic range compression, synthetic aperture compounding, and frequency compounding.
    *   Speckle-reduction filtering, edge-enhancement kernels, and directional tissue smoothing.

![Adaptive Filtering and Phantom Evaluation](../images/projects/ultrasound/ImageFilters.PNG)
*Figure 2: Multi-parameter image tuning, spatial compounding, and tissue phantom evaluation across single- and multi-viewport layouts.*

---

## 3. Comprehensive Imaging Modalities

The system supports multi-probe array geometries and full-spectrum clinical imaging modalities:

![Multimodal Imaging Showcase](../images/projects/ultrasound/OtherModalities.PNG)
*Figure 3: Multi-modality clinical captures: (Top-Left) Convex Anatomical M-mode; (Top-Right) Sector Color Flow Doppler; (Bottom-Left) Trapezoid Duplex; (Bottom-Right) Linear Pulsed Wave Doppler (PWD).*

### Modality Engineering Highlights
*   **Cardiac & Hemodynamic Analysis:** Phased-array sector B-mode, high-pulse-repetition-frequency (PRF) Puls contrast.
    *   **Short-Lag Spatial Coherence (SLSC):** Coherence-based imaging minimizing clutter and acoustic reverberation artifacts.
*   **Real-Time Post-Processing & Filtering:**
    *   Dynamic range compression, synthetic aperture compounding, and frequency compounding.
    *   Speckle-reduction filtering, edge-enhancement kernels, and directional tissue smoothing.

![Adaptive Filtering and Phantom Evaluation](../images/projects/ultrasound/ImageFilters.PNG)
*Figure 2: Multi-parameter image tuning, spatial compounding, and tissue phantom evaluation across single- and multi-viewport layouts.*

---

## 3. Comprehensive Imaging Modalities

The system supports multi-probe array geometries and full-spectrum clinical imaging modalities:

![Multimodal Imaging Showcase](../images/projects/ultrasound/OtherModalities.PNG)
*Figure 3: Multi-modality clinical captures: (Top-Left) Convex Anatomical M-mode; (Top-Right) Sector Color Flow Doppler; (Bottom-Left) Trapezoid Duplex; (Bottom-Right) Linear Pulsed Wave Doppler (PWD).*

### Modality Engineering Highlights
*   **Cardiac & Hemodynamic Analysis:** Phased-array sector B-mode, high-pulse-repetition-frequency (PRF) Puls, Vascular, Abdominal, Nerve, and Small Parts presets.
*   **Integrated Annotation Matrix:** Vector-rendered body markers, probe orientation indicators, and standardized clinical measurement packages.

---

## 6. Review Station, DICOM Archival & Structured Reporting

The software includes a PACS-compliant review station and database management subsystem for clinical workflow integration.

![DICOM Review, Multi-Frame Playback, and Clinical Reports](../images/projects/ultrasound/Storing.PNG)
*Figure 7: Clinical study review workflow: (Top-Left) Patient study directory and media management; (Top-Right) Structured clinical report editor; (Bottom) Single-frame and 4-up synchronized cine playback.*

*   **PACS & DICOM 3.0 Compliance:** Native DICOMDIR parsing, Worklist management, Store SCU, and structured export.
*   **Multi-View Cine Review:** Multi-viewport comparison matrix (Single, Dual, Quad layouts) with dynamic zoom, pan, and post-freeze measurements.
*   **Structured Reporting:** Automated transfer of biophysical calculations, hemodynamic parameters, and clinician impressions into printable and exportable reports.

---

## 7. Technology Stack Summary

*   **Hardware / Front-End:** Analog Front-End (AFE), High-Voltage Pulsers, T/R Switches, Custom FPGA Acquisition Boards.
*   **Compute & Algorithms:** C++, CUDA, MATLAB (Prototyping), SIMD Optimizations, OpenGL/Vulkan rendering.
*   **Application & UI Framework:** Qt 5/6, QML, C++, Linux (Ubuntu Real-Time Kernel), Android (Handheld platform).
*   **Standards & Protocols:** DICOM 3.0, IHE Radiology/Cardiology profiles, Medical Device Safety & Usability standards.

