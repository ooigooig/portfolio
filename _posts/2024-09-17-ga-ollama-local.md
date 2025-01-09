---
layout: post
title: Gen AI:Use local ollama
date: 2024-09-17 16:40:16
description: 
tags: GenerativeAI
categories: SimpleGenAIproject
giscus_comments: true
---



{::nomarkdown}
{% assign jupyter_path = 'assets/jupyter/use_local_ollama.ipynb' | relative_url %}
{% capture notebook_exists %}{% file_exists assets/jupyter/use_local_ollama.ipynb %}{% endcapture %}
{% if notebook_exists == 'true' %}
  {% jupyter_notebook jupyter_path %}
{% else %}
  <p>Sorry, the notebook you are looking for does not exist.</p>
{% endif %}
{:/nomarkdown}