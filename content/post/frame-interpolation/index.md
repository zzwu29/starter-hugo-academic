---
title: Frame Interpolation
subtitle: interpolation of images and videos
# Summary for listings and search engines
summary: interpolation of images and videos
# Link this post with a project
projects: []

# Date published
date: '2023-10-11T00:00:00Z'

# Date updated
lastmod: '2023-10-11T00:00:00Z'

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
  - computer vision
categories:
  - research
---

## Introduction

When I tried to solve a state estimation via visual-inertial odometry, I found that the some photos captured by camera were lost.

## Open-source Project

- https://film-net.github.io/
- https://github.com/google-research/frame-interpolation


## Paper

https://arxiv.org/pdf/2202.04901

## Scripts

[Download](./img_proc.zip)

## Problem

- significant linear motion
- turn a corner
- frame interval too long (>= **0.2s** in autonomous driving)