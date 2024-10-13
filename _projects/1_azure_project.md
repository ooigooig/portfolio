---
layout: page
title: Azure Data Factory:Covid19 data in Data Ingestion and Data Flows
description: 
img: assets/img/azure/homepage.jpg
importance: 1
giscus_comments: true

---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/azure/all_resources.png" title="all_resources" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Azure interface: all resources
</div>

This project focuses on using **Azure Data Factory (ADF)** to manage and process COVID-19 data. As you can see in this screenshot of the Azure interface, there are several components: **ADF, Azure SQL database, Azure Databricks, Log Analytics Workspace, etc**. These resources align with a **data pipeline architecture**, combining ADF for ETL, SQL for structured storage, and Databricks for analytics.

**<mark>Framework/Architecture of this project </mark>**

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/azure/framework.png" title="framework" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/azure/architecture.png" title="architecture" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


**<mark>Data Flow</mark>**

The first data flow(transform hospital admissions) focused on aggregating hospital admissions data, conditionally splitting it into weekly and daily data streams, applying transformations such as pivoting and sorting, and exporting the processed data into destination sinks.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/azure/data_flow.png" title="data_flow" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Data Flow: transform hospital admissions
</div>

The second data flow(transform cases deaths) filtered case and death data specifically for Europe, performed lookups to enrich country-level information, and aggregated the data before exporting it to the final dataset. Key components included pivot transformations, conditional splitting, lookups, and sorting, which ensured efficient data organization and readiness for reporting and analysis.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/azure/data_flow2.png" title="data_flow2" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Data Flow: transform cases deaths
</div>

**<mark>Some problem when I was doing this project:</mark>**
1. <mark>Parameters & Variables</mark>
  

Parameters are external values passed into pipelines, datasets or linked services. The value cannot be changed inside a pipeline.
Variables are internal values set inside a pipeline. The value can be changed inside the pipeline using Set Variable or Append Variable Activity.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/azure/parameter.png" title="parameter" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

If we want to ingest http/url in the json file, we need to set them in the variables.


2. <mark>website column name changed</mark>
  
The data of the website keeps updating and the column and row change every day, I did the project in 2022, but now the ingested files column names are changed.

3. wrong name reulted in null data
  

I am confused that why the confirmed cases column is null with all rows...But I found that I did something really silly: co~~m~~nfirmed


<div class="row justify-content-sm-center">
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/azure/wrong_confirmed1.png" title="wrong_confirmed1" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/azure/wrong_confirmed2.png" title="wrong_confirmed2" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Finally!!

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/azure/wrong_confirmed3.png" title="wrong_confirmed3" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

4. unable to access Azure HDInsight

Unfortunately, I cannot create the Azure HDInsight cluster with the Student subscription. :(

[Reason: With an Azure Student subscription, you will initially be able to access only Azure services that are available with a free tier of service use.](https://learn.microsoft.com/en-us/answers/questions/179055/can-i-use-a-student-subscription-in-azure-to-creat)

5. unable to have permission for access tokens to access the databricks REST API

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/azure/databricks.png" title="databricks" class="img-fluid rounded z-depth-1" %}
    </div>
</div>