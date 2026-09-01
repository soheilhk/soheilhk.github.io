---
title: "Data-Subset Stability (DSS)-Guided Artifact Suppression for 
Ultrasound Tomography (Under Review)"
collection: publications
category: manuscripts
permalink: /publication/Paper_Journal_Hakakzadeh_et_al_DSS_RUCT
excerpt: "A Data-Subset Stability (DSS) framework for sparse-transmit reflection ultrasound computed tomography (RUCT) that estimates pixel-wise stability across partitioned transmit events. Validated on point-source, three-circle, and in-vivo mouse datasets across sparsity factors 1 to 16, DSS achieves up to 19 dB SNR gain and a ~5 dB reduction in in-vivo background fluctuations."
date: 2026-12-19
authors: "S Hakakzadeh, M Mehrmohammadi"
venue: ''
slidesurl: 'https://academicpages.github.io/files/slides2.pdf'
paperurl: ''
publisherurl: ''
citation: ''
---
Abstract
 Reflection ultrasound computed tomography (USCT) enables high-resolution cross-sectional imaging; however, sparse
transmit acquisition required for high-frame-rate imaging introduces severe artifacts that degrade image quality. This paper introduces 
a Data-Subset Stability (DSS) framework that estimates reconstruction stability from independently reconstructed subsets of the 
acquired data. In reflection USCT, these subsets are formed by partitioning the transmit events into independent groups. Because 
genuine reflectors exhibit consistent responses across independent data subsets, whereas artifacts vary with acquisition geometry, 
reconstruction stability provides an effective criterion for distinguishing true structures from artifacts. A pixel‑wise stability map 
estimated from inter-subset consistency analysis is used as a spatial weighting map to reinforce consistent reflectors while attenuating 
incoherent artifact contributions. The proposed framework was validated using a point-source phantom, a three-circle phantom, as 
well as in-vivo mouse datasets across transmit sparsity factors ranging from 1 to 16. Experimental results demonstrate that the proposed 
DSS framework significantly outperforms conventional synthetic aperture focusing technique (SAFT) reconstruction. In phantom 
experiments, the proposed method achieved up to 19 dB improvement in signal‑to‑noise ratio (SNR) and substantial artifact reduction, 
maintaining high contrast‑to‑noise ratio (CNR) even under strong transmit sparsity. In‑vivo results further confirmed the robustness 
of the approach, showing a ~5 dB reduction in background fluctuations and improved preservation of tissue interfaces. Because the 
proposed framework operates entirely during image reconstruction, it can be integrated into existing reflection USCT reconstruction 
pipelines without modifications to the acquisition hardware or imaging protocol. 
