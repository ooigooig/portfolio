---
layout: page
title: Sentiment Analysis on Movie Reviews:A predictive model with pre-trained Bert by PyTorch
description: 
img: assets/img/nn_project/homepage.png
importance: 1

giscus_comments: true
---

[[Code]](https://howardzhan2024.top/assets/html/sentiment_analysis_pt_Huaye-final.html) [[PPT]](https://howardzhan2024.top/assets/pdf/neural_networks_pytorch_Huaye.pdf) [[Demo]](https://howardzhan2024.top/assets/video/sentiment_analysis_demo.mp4)



In this project,

**Kaggle API**

I need to set up the configuration in my desktop.

**Transfer learning and fine tuning**

What is Transfer learning and fine-tuning?

Transfer learning is a general machine learning technique that is not specific to transformers or their architecture. It is applied to transformers to make them practical and useful, significantly reducing the cost and effort required to train them. Without transfer learning, training a transformer would be prohibitively expensive.

Fine-tuning is a Fine-tuning is a transfer learning technique where I take a pre-trained model (like BERT, which has been trained on a large amount of general text data) and further train it on a specific task or dataset while leveraging its pre-learned knowledge.

<u>When I first learned about transfer learning and fine-tuning, a few questions came to mind:</u>

1. *Do only the new layers need to be trained during transfer learning?*
  
2. *how can I fine-tuning the pre-trained model without training it?*
  
3. *If I fine-tune the entire model, is it still different from training the pre-trained model from scratch?*