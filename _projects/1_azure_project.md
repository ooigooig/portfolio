---
layout: page
title: Azure Data Factory:Covid19 data in Data Ingestion and Data Flows
description: 
img: assets/img/azure/homepage.jpg
importance: 1
giscus_comments: true

---


**<mark>Framework of this project </mark>**
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/azure/framework.png" title="framework" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    framework
</div>

**<mark>Architecture of this project </mark>**

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/azure/architecture.png" title="architecture" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    architecture
</div>

This project focuses on using **Azure Data Factory (ADF)** to manage and process COVID-19 data. As you can see in this screenshot of the Azure interface, there are several components: **ADF, Azure SQL database, Azure Databricks, Log Analytics Workspace, etc**. These resources align with a **data pipeline architecture**, combining ADF for ETL, SQL for structured storage, and Databricks for analytics.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/azure/all_resources.png" title="all_resources" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Azure interface: all resources
</div>


Unfortunately, I cannot create the Azure HDInsight cluster with the Student subscription. :(

[Reason: With an Azure Student subscription, you will initially be able to access only Azure services that are available with a free tier of service use.](https://learn.microsoft.com/en-us/answers/questions/179055/can-i-use-a-student-subscription-in-azure-to-creat)
