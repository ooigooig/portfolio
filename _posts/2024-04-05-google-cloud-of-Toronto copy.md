---
layout: post
title: MySQL Triggers Syntax
date: 2024-06-16 16:40:16
description: 
tags: Google
categories: activity
---



```sql
CREATE TRIGGER trigger_name
{BEFORE|AFTER}{INSERT|UPDATE|DELETE}
ON table_name FOR EACH ROW
{{FOLLOW|PRECEDES} existing_trigger_name}
[[some statement we want to execute by trigger]]
{WHERE column_name ={OLD|NEW}.column_name}
```