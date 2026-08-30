---
layout: research-category
title: "Echocardiography"
permalink: /research/echo/ 
author_profile: true

badge_icon: "fa-solid fa-heart-pulse"
badge_text: "Cardiovascular Ultrasound"
hero_title: "Echocardiography & Cardiac Strain Imaging"
hero_desc: "Advancing real-time cardiac ultrasound diagnostics through GPU-accelerated speckle tracking, high-frame-rate plane-wave imaging, and deep learning-based automated view classification."

projects:
  - title: "Automated Left Ventricular Strain & Speckle Tracking"
    summary: "Real-time 2D Lagrangian strain estimation for ischemic border identification."
    featured: true
    tags: 
      - "Speckle Tracking"
      - "Myocardial Strain"
      - "CUDA/C++"
    image: "/images/research/echo-strain.jpg"
    caption: "Fig 1. Automated endocardial contouring and segmental longitudinal strain curves."
    body_html: |
      Quantification of regional myocardial mechanics via speckle tracking echocardiography (STE) provides sensitive diagnostic metrics prior to manifest ejection fraction degradation.
      
      We developed a high-throughput block-matching algorithm optimized on NVIDIA Tensor Cores that computes global longitudinal strain (GLS) and radial strain tensors at >120 frames per second. The pipeline incorporates an elastographic quality metric to eliminate decorrelated out-of-plane tracking artifacts.
    paper: "https://doi.org/"
    code: "https://github.com/soheilhk/EchoApp"

  - title: "Deep Learning for Standard Echocardiographic View Classification"
    summary: "Multi-view video spatio-temporal network for real-time apical and parasternal view detection."
    tags: 
      - "Deep Learning"
      - "Video CNN"
      - "EchoApp"
    image: "/images/research/echo-ai.jpg"
    caption: "Fig 2. Spatio-temporal ResNet-3D architecture for 8-view classification."
    body_html: |
      Point-of-care cardiac ultrasound (POCUS) adoption is hindered by high operator dependency. We designed a lightweight spatio-temporal deep network capable of classifying standard views (A2C, A4C, PLAX, PSAX) in B-mode video cineloops in real-time on edge compute units.
    paper: "https://doi.org/"
    code: "https://github.com/soheilhk"
---
