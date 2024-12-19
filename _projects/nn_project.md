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

<div class="row justify-content-sm-center">

    <div class="col-sm mt-3 mt-md-0">

        {% include figure.liquid loading="eager" path="assets/img/nn_project/kaggle_api.png" title="excel" class="img-fluid rounded z-depth-1" %}

    </div>

</div>
<div class="caption">
    clicking create new token, and downloading the configuration file.
</div>


<div class="row justify-content-sm-center">

    <div class="col-sm mt-3 mt-md-0">

        {% include figure.liquid loading="eager" path="assets/img/nn_project/kaggle_setup.png" title="excel" class="img-fluid rounded z-depth-1" %}

    </div>

</div>
<div class="caption">
    I need to set up the configuration in my desktop.
</div>

<div class="row justify-content-sm-center">

    <div class="col-sm mt-3 mt-md-0">

        {% include figure.liquid loading="eager" path="assets/img/nn_project/kaggle_code.png" title="excel" class="img-fluid rounded z-depth-1" %}

    </div>

</div>
<div class="caption">
    Finally, I can fetch dataset in Kaggle through kaggle api.
</div>


**Transfer learning and fine tuning**

What is Transfer learning and fine-tuning?

Transfer learning is a general machine learning technique that is not specific to transformers or their architecture. It is applied to transformers to make them practical and useful, significantly reducing the cost and effort required to train them. Without transfer learning, training a transformer would be prohibitively expensive.

Fine-tuning is a Fine-tuning is a transfer learning technique where I take a pre-trained model (like BERT, which has been trained on a large amount of general text data) and further train it on a specific task or dataset while leveraging its pre-learned knowledge.

<u>When I first learned about transfer learning and fine-tuning, a few questions came to mind:</u>

1. *Do only the new layers need to be trained during transfer learning?*
  
2. *how can I fine-tuning the pre-trained model without training it?*
  
3. *If I fine-tune the entire model, is it still different from training the pre-trained model from scratch?*
  

When I fine-tune the entire model, I am still leveraging the pre-trained weights and representations from the original BERT model. The key difference is that I am allowing those pre-trained layers to be updated during the fine-tuning process, rather than keeping them completely frozen.

Training the pre-trained BERT model from scratch would involve randomly initializing all the model parameters and training the entire model on a large, general-purpose dataset (like the dataset used to originally pre-train BERT) to learn the base language representations.

<u>The key lies in either <strong>initializing</strong> or <strong>optimizing</strong> model parameters. I don't need to train <strong>pre</strong>-trained model since it is already trained.</u>

<div class="row justify-content-sm-center">

    <div class="col-sm mt-3 mt-md-0">

        {% include figure.liquid loading="eager" path="assets/img/nn_project/tl_ppt.png" title="excel" class="img-fluid rounded z-depth-1" %}

    </div>

</div>

**Conclusion**

In conclusion, the demo performs well, but the accuracy is approximately 70%. There is room for improvement in the model.

1. Train more epochs to observe the result.✅
  

Result: Overfitting😂

Reason: I fine-tune the entire model, include pre-trained model.

How to improve: I should fine-tune a few layers of the pre-trained model first, and see the result.