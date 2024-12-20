---
layout: page
title: KSI-Related Collisions in Toronto:A predictive model with an app
description: 
img: assets/img/ksi_toronto/ksi_homepage.png
importance: 4

giscus_comments: true
---

[[Code]](https://howardzhan2024.top/assets/html/group_project_Huaye-final_code.html) [[Dataset]](https://data.torontopolice.on.ca/datasets/0a1ee9d9436546dcbdc0ee9301e45e83_0/explore) [[PPT]](https://howardzhan2024.top/assets/pdf/predictive_model_with_an_app.pdf)

This project involves building a predictive model using the Killed or Seriously Injured (KSI) collision dataset provided by the Toronto Police Service. The goal is to predict whether an individual involved in a collision is fatal or non-fatal based on their specific information.

The main challenge of this project lies in the dataset itself, as the fatal or non-fatal classification is based on the overall accident rather than the individual person involved.

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/ksi_toronto/data_cleaning.png" title="ksi_toronto" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

In a traffic accident, multiple individuals may be involved, each associated with different vehicles. However, how does the dataset classify an accident as fatal or non-fatal? Typically, it is categorized as fatal if at least one person dies. If we aim to build a model to predict whether an individual’s outcome is fatal or non-fatal, we need to exclude all individuals incorrectly marked as fatal. These individuals are labeled as such solely because the accident was fatal, even though they themselves did not die.

