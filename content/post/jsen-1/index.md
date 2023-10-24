---
title: A work on indoor-outdoor positioning
subtitle: PPP/INS/UWB tightly coupled integration

# Summary for listings and search engines
summary: PPP/INS/UWB tightly coupled integration

# Link this post with a project
projects: []

# Date published
date: '2023-08-28T00:00:00Z'

# Date updated
lastmod: '2023-08-28T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: ''
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - admin
tags: 
  - seamless positioning
  - sensor fusion
categories:
  - research
---

## Title

An indoor and outdoor seamless positioning system for low-cost UGV using PPP/INS/UWB tightly coupled integration

Published in: IEEE Sensors Journal

## Author

Xingxing Li, Zongzhou Wu, Zhiheng Shen, Zhili Xu, Xin Li, Shengyu Li and Junjie Han

# Abstract

Seamless positioning is critical for mobile robots to achieve ubiquitous availability in all scenarios. Precise point positioning (PPP) technique provides a centimeter-level solution without a reference station and is often integrated with an inertial navigation system (INS) for outdoor navigation of unmanned ground vehicles (UGVs). However, in challenging environments such as indoors, the performance of PPP/INS systems is severely degraded, while ultra-wideband (UWB) is widely used due to its high accuracy over short distances. This paper proposes a tightly coupled PPP/INS/UWB integrated system, in which satellite-difference ionosphere-free pseudorange and carrier-phase measurements from a single receiver, micro-electro-mechanical system (MEMS) inertial measurements, and the UWB rangings are tightly fused to accomplish continuous and precise positioning throughout indoor and outdoor coverage. To mitigate the effects of non-line-of-sight (NLOS), multipath and faulty signals, a two-step weighting approach is proposed to improve UWB positioning performance, including segmentation weighting based on the signal strength, and weight adjustment based on area identification. Besides, motion constraints are imposed on velocity, yaw, and height to suppress drifts during signal-harsh periods. Real-world experiment results show that the proposed system can achieve continuous positioning in the overall indoor and outdoor environments, with the MAEs of (0.214 m, 0.186 m, 0.243 m) and the RMSEs of (0.339 m, 0.291 m, 0.414 m) in the east, north, and up directions. In transitional areas with severe signal interference and interruption, a 0.5 m positioning accuracy and smooth switching are still attainable.

## Keyword

Area identification, micro-electro-mechanical system, multisensor fusion, precise point positioning, seamless positioning, tightly coupled integration, ultra-wideband

## DOI

10.1109/JSEN.2023.3310480

## Link

https://ieeexplore.ieee.org/document/10242329
