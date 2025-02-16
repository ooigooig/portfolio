---
layout: post
title: gitlab CI/CD
date: 2024-06-31 16:40:16
description: 
tags: CI/CD
categories: note
giscus_comments: true
---


**1.What is a pipeline?**

A pipeline is a series of connected steps, similar to an assembly line in a car factory, where each step must be done in a specific order to build a final product. In a pipeline:

- Each step’s output becomes the next step's input.
- Some steps, like adding wheels, can be done in parallel.
- Numerous steps are required, from initial assembly to final testing, to ensure quality before delivering to the customer.

**2.GitLab's architecture:**

- A **GitLab Server** provides the interface and stores repositories but delegates job execution to **GitLab Runners**.
- This separation allows GitLab to scale efficiently, as the server doesn’t run jobs directly.
- Runners, found under **Settings > CI/CD > Runners** in each project, execute pipeline jobs. GitLab.com offers **Shared Runners**, but users can also set up custom Runners on their infrastructure and assign them to specific projects for more tailored control.

**3.Why GitLab/GitLab CI?**

GitLab is a modern tool positioned to become a market leader. It offers:

- A scalable, modern architecture
- Easy integration with Docker
- Pipeline-as-code capabilities
- A partially open-source model

**4.What is CI/CD?**

- **CI (Continuous Integration)**: A development practice where code changes are frequently integrated with the work of other developers. CI includes:
  
  - Verifying builds and running unit tests
  - Ensuring adherence to coding guidelines
  - Integrating code multiple times per day
  - Producing a deployable package
- **CD (Continuous Delivery)**: Follows CI and focuses on testing the package created by CI to prepare it for production:
  
  - Tests the installability and compatibility of the package in a production-like environment
  - Requires manual approval before deploying to production
- **CD (Continuous Deployment)**: Extends Continuous Delivery by automatically deploying every tested package to production without manual intervention, provided it passes all previous stages.
  

**5.Advantages of CI:**

- Detects errors early in development
- Reduces integration issues
- Enables faster development pace

**6.Advantages of CD:**

- Ensures every change is ready for release
- Lowers deployment risk
- Speeds up value delivery with more frequent releases

**7.What is Docker?**

Docker is a virtualization tool that uses **images**—pre-configured software environments with all necessary dependencies.

- **Images**: Files with instructions to package code, tools, and dependencies.
- **Containers**: Executed images, functioning similarly to virtual machines but are lighter.

In traditional CI servers, dependencies are installed directly on the server. However, **GitLab CI** utilizes Docker images for dependency management, allowing **GitLab CI Runners** to use specified images, simplifying and scaling the setup.

**8.Why Do Jobs Fail?**

Jobs fail due to command exit codes:

- **0**: Command executed successfully
- **>0**: Command failed

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/gitlab/job_fail.png" title="job_fail" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


**9.Cache vs Artifacts**

Though similar, **caches** and **artifacts** serve different purposes in CI/CD:

- **Artifacts**:
  
  - Outputs from the build process (e.g., deployable packages).
  - Can be partial outputs if built across stages.
  - Used to pass data between jobs or stages.
- **Cache**:
  
  - Temporary storage for project dependencies.
  - Not intended for storing artifacts, even if possible.

For more details, refer to [GitLab documentation](https://docs.gitlab.com/ee/ci/caching/#cache-vs-artifacts).