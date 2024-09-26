---
layout: post
title: Contractive loss
date: 2024-09-25 16:40:16
description: 
tags: Q&A
categories: neural networks
giscus_comments: true
---

- Contrastive Loss is a distance-based Loss function (as opposed to **prediction error-based** losses like cross entropy) used to learn discriminative features for images.
- Like any distance-based loss, it tries to ensure that semantically similar examples are embedded close together. It is calculated on **Pairs**
- This loss measures the *<mark>similarity</mark>* between two inputs.
- Each sample is composed of two images (*<mark>positive pairs</mark>* or *<mark>negative pairs</mark>*). Our goal is to maximize the distance between *<mark>negative pairs</mark>* and <u>minimize</u> the distance between <mark>*positive pairs*</mark>.
- We want small distance between the positive pairs (because they are similar images/inputs), and great distance than some margin m for negative pairs.