---
layout: post
title: EER diagrams and database tables
date: 2024-09-25 16:40:16
description: 
tags: Q&A
categories: SQL
giscus_comments: true
---

important concept regarding **EER diagrams** and **their synchronization with database tables**

I added two foreign keys to the customer purchases diagram, but when checking the actual table, the foreign keys were not added. The key takeaway is that updating the ETR diagram does not automatically synchronize changes with the tables in the schema. So we will be working directly in the tables and using reverse engineering to update the ETR diagram for an accurate snapshot, rather than expecting changes in the diagram to reflect in the database.