---
layout: post
title: Is KL divergence same as cross entropy for image classification?
date: 2024-08-23 16:40:16
description: 
tags: Q&A
categories: neural networks
giscus_comments: true
---


**<mark><u>Yes</u></mark>**

In Image classification, we use one-hot encoding for our labels. Therefore, when y_i is the actual label, it equals 1 → log (1) = 0, and the whole term is cancelled. When y_i is not the correct label, it equals 0 and the whole term is also cancelled out.

Therefore, KL divergence = Cross Entropy in image classification tasks

