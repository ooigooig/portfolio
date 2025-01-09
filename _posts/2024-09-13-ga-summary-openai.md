---
layout: post
title: Gen AI:Summary my portfolio by OpenAI
date: 2024-09-13 16:40:16
description: 
tags: GenerativeAI
categories: SimpleGenAIproject
giscus_comments: true
---



{::nomarkdown}
{% assign jupyter_path = 'assets/jupyter/summary_my_portfolio.ipynb' | relative_url %}
{% capture notebook_exists %}{% file_exists assets/jupyter/summary_my_portfolio.ipynb %}{% endcapture %}
{% if notebook_exists == 'true' %}
  {% jupyter_notebook jupyter_path %}
{% else %}
  <p>Sorry, the notebook you are looking for does not exist.</p>
{% endif %}
{:/nomarkdown}