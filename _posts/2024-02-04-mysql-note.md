---
layout: post
title: MySQL Syntax
date: 2024-09-25 16:40:16
description: 
tags: MySQL
categories: note
giscus_comments: true
---

**Trigger**

**<mark>CREATE TABLE W/ CODE</mark>**

```sql
USE myfirstcodeschema;

CREATE TABLE myfirstcodetable (
    myfirstcodetable_id BIGINT NOT NULL,
    my_character_field VARCHAR(50),
    my_text_field TEXT,
    my_created_at TIMESTAMP
);
```

**<mark>INSERTING NEW RECORDS</mark>**

```sql
USE thriftshop;

SELECT * FROM inventory;

INSERT INTO inventory (inventory_id, item_name, number_in_stock) VALUES(10,'wolf skin hat', 1);
```

(Another) :

```sql
INSERT INTO inventory VALUES
(11,'fur fox skin',1),
(12,'plaid button up shirt',8),
(13,'flannel zebra jammies',6);
```

**<mark>DELETE RECORDS</mark>**

```sql
DELETE FROM inventory
WHERE inventory_id = 7
```

**<mark>IMPORT DATA FROM A FILE</mark>**

```sql
CREATE SCHEMA survey;

USE survey;

CREATE TABLE salary_survey (
    country VARCHAR(50),
    years_experience INT,
    employment_status VARCHAR(50),
    job_title VARCHAR(50),
    is_manager VARCHAR(50),
    education_level VARCHAR(50),
    );
```

**<mark>ALTER TABLE W/ CODE</mark>**

```sql
SELECT * FROM customer_purchases;

ALTER TABLE customer_purchases
DROP COLUMN 


ALTER TABLE customer_purchases
ADD COLUMN purchase_amount DECIMAL(6,2) AFTER customer_purchase_id;


SELECT * FROM customer_purchases;
```

**<mark>UPDATING RECORDS</mark>**

```sql
UPDATE inventory
SET number_in_stock = 0;
WHERE inventory_id = 9;
```

(Another) :

```sql
UPDATE inventory
SET number_in_stock = 0
WHERE inventory_id IN(1,9);
```

**<mark>TRIGGERS HELPFUL HINTS:</mark>**

```sql
CREATE TRIGGER trigger_name
<BEFORE|AFTER><INSERT|UPDATE|DELETE>
ON table_name FOR EACH ROW
<<FOLLOW|PRECEDES> existing_trigger_name>
<<some statement we want to execute by trigger>>
<WHERE column_name =<OLD|NEW>.column_name>
```
------------------------------------------------------------------

**EER diagrams and database tables**


important concept regarding **EER diagrams** and **their synchronization with database tables**

I added two foreign keys to the customer purchases diagram, but when checking the actual table, the foreign keys were not added. The key takeaway is that updating the ETR diagram does not automatically synchronize changes with the tables in the schema. So we will be working directly in the tables and using reverse engineering to update the ETR diagram for an accurate snapshot, rather than expecting changes in the diagram to reflect in the database.