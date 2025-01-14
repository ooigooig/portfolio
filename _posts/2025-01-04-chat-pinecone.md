---
layout: post
title: Gen AI:RAG Q&A Conversation With PDF Including Chat History
date: 2025-01-03 16:40:16
description: 
tags: GenerativeAI
categories: SimpleGenAIproject
giscus_comments: true
---

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/post/pinecone.png" title="pinecone" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

{::nomarkdown}
{% assign jupyter_path = 'assets/jupyter/chatbot-pinecone.ipynb' | relative_url %}
{% capture notebook_exists %}{% file_exists assets/jupyter/chatbot-pinecone.ipynb %}{% endcapture %}
{% if notebook_exists == 'true' %}
  {% jupyter_notebook jupyter_path %}
{% else %}
  <p>Sorry, the notebook you are looking for does not exist.</p>
{% endif %}
{:/nomarkdown}  