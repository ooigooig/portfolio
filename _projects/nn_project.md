---
layout: page
title: Sentiment Analysis on Movie Reviews:A predictive model with pre-trained Bert by PyTorch
description: 
img: assets/img/nn_project/homepage.png
importance: 1

giscus_comments: true
---

[[Code]](https://howardzhan2025.top/assets/html/sentiment_analysis_pt_Huaye-final.html) [[PPT]](https://howardzhan2025.top/assets/pdf/neural_networks_pytorch_Huaye.pdf) [[Demo]](https://howardzhan2025.top/assets/video/sentiment_analysis_demo.mp4)

In this project, I explored sentiment analysis on movie reviews using a predictive model powered by a pre-trained BERT model implemented with PyTorch. BERT’s ability to understand context makes it perfect for analyzing and predicting sentiment in movie reviews.

**Kaggle API**

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/nn_project/kaggle_api.png" title="kaggle_api" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    clicking create new token, and downloading the configuration file.
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/nn_project/kaggle_setup.png" title="kaggle_setup" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    I need to set up the configuration in my desktop.
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/nn_project/kaggle_code.png" title="kaggle_code" class="img-fluid rounded z-depth-1" %}
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

💡<u>The key lies in either <strong>initializing</strong> or <strong>optimizing</strong> model parameters. I don't need to train <strong>pre</strong>-trained model since it is already trained.</u>

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/nn_project/tl_ppt.png" title="excel" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

**Conclusion**

In conclusion, the demo performs well, but the accuracy is approximately 70%. There is room for improvement in the model.

1.Train more epochs to observe the result.✅

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/nn_project/more_epoch.png" title="excel" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Result: Overfitting😂

Reason: I fine-tune the entire model, include pre-trained model.

How to improve: I should fine-tune a few layers of the pre-trained model first, and see the result.

2.Model comparison: compared with other pre-training models.🕚

There are many other bert or pre-trained models used for text classification in huggingface platform.

3.Data binning and Data processing: bin 0 into 1, bin 3 into 4, to make the data less imbalanced in preprocessing data.🕥

<div class="row justify-content-sm-center">
    <div class="col-sm-7 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/nn_project/data_bining.png" title="data_bining" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

For example, we can bin the 8 clarity values into just 3 distinct buckets( In this project, I bin 0 and 1 into negative, 3 and 4 into positive.)

As we know well, Adding dummy variables(aka. one-hot encoder) is a technique as well.

💡**In my opinion, adding dummy variables for each categorical column can lead to wide data sets and increase model variance; binning can solve this and improve interpretability.**