---
layout: post
title: Why cross entropy comes in hand with Softmax layer?
date: 2024-06-16 16:40:16
description: 
tags: Q&A
categories: neural networks
---


**<mark><u>Why we need to use softmax function after cross entropy?</u></mark>**

Because thecross entropy loss takes the logatithm of the probability. So in order to compute an efficient logarithm, we need to have a probability distribution that sums up to 1.