---
permalink: /contact/
author_profile: true
---
# autoStrain: AI-Powered Echocardiography Analysis Platform

**autoStrain** is an advanced clinical workstation software designed for automated cardiac function assessment from 2D echocardiography cine loops. Built with a high-performance C++/Qt/QML front-end and a deep learning backend, it streamlines echocardiographic workflows by providing automated view classification, myocardial border delineation, speckle tracking deformation analysis, volumetric assessment, and structured clinical reporting.

---

## 1. System Architecture & End-to-End Pipeline

The clinical pipeline follows a structured, two-phase modular workflow that balances full automation with mandatory clinician verification at critical decision points:

*   **Phase 1: Acquisition & Anatomical Delineation**
    *   **DICOM Ingestion:** Multi-series PACS integration, metadata extraction, and local directory indexing.
    *   **AI View Detection:** Deep convolutional neural network for acoustic view classification (A4C, A2C, A3C, short-axis views) and ECG-synchronized R-wave cardiac cycle gating.
    *   **AI Myocardial Segmentation:** Automated multi-point tracking of endocardial and epicardial borders with automatic identification of End-Diastole (ED) and End-Systole (ES) frames.
    *   **Clinician Review & Interactive Approval:** Manual contour adjustment mode ensuring clinical oversight before deformation computation.
*   **Phase 2: Mechanics Quantification & Clinical Reporting**
    *   **AI Speckle Tracking:** Dense optical flow and feature-tracking algorithms to quantify myocardial tissue deformation frame-by-frame.
    *   **Automated Strain Quantification:** Segmental time-strain curves, Global Longitudinal Strain (GLS), and anatomical curved M-mode colormaps.
    *   **Volumetric Assessment:** Automated Biplane Simpson’s disc summation for LV volumes (EDV, ESV, SV) and Ejection Fraction (LVEF).
    *   **Clinical Reporting & Polar Maps:** AHA 17-segment polar bullseye maps (peak strain and time-to-peak dyssynchrony) alongside structured PACS/PDF reporting.



---
