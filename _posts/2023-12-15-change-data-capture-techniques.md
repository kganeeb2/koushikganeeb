---
layout: post
title:  "Change Data Capture Techniques"
summary: "Change Data Capture Techniques"
author: kganeeb
date: '2023-12-15 14:35:23 +0530'
keywords: Data Capture, Databases, SQL, CDC, Incremental, Full
permalink: /blog/change-data-capture-techniques/
usemathjax: true
---

 <img src="/assets/img/posts/change-data-capture-techniques.png" class="img-fluid">
 
## Change Data Capture:

Change Data Capture (CDC) is a technique used in databases to identify and track changes to data. It’s particularly valuable in scenarios where you need to capture and process only the data that has been modified, added, or deleted since the last update. Here are different types of Change Data Capture techniques.
  

## 1.Timestamp-Based CDC:
In this technique, a timestamp column is added to each record in the table. When a record is updated, the timestamp is modified. During CDC processing, records with timestamps greater than the last processing timestamp are considered as changes.

## 2.Log-Based CDC:
Utilizes the database transaction log to capture changes. As changes are made to the database, they are recorded in the transaction log. The CDC process reads the log to identify changes.

## 3.Incremental Loading with High-water Mark:
In this technique, a high-water mark (e.g., a unique identifier or timestamp) is used to identify the point up to which data has been processed. During CDC, only records with identifiers greater than the high-water mark are processed.

## 4.Triggers-Based CDC:
Database triggers are used to capture changes to tables. Triggers are set to execute on INSERT, UPDATE, and DELETE operations, and they insert records into a CDC table.

## 5.Hash-Based CDC:
A hash value (checksum) is computed for each record. During CDC, the hash values are compared, and if they differ, the record is considered changed.

## 6.Database Replication CDC:
Replication tools replicate changes from a source database to a target database. Changes include inserts, updates, and deletes.

## 7.Database Query-Based CDC:
Periodic queries are run on the database to identify changes. For example, a query might identify records modified or added in the last hour.

## 8.Change Tracking Tables:
An additional table is maintained to track changes to the main table. For each change, a record is inserted into the change tracking table.

## 9.Message Queue-Based CDC:
Changes are captured as events and sent to a message queue. Subscribers to the queue process these events.

## 10.Periodic Full Data Load with Delta Tables:
Periodically, the entire table is loaded. A delta table is used to store changes made since the last full load.

## 11. Bi-Temporal Tables:
Bi-temporal tables include two time dimensions, capturing both the system time and transaction time. They provide more information about when the data was valid and when changes occurred.

When choosing a CDC technique, consider factors such as the volume of data changes, performance implications, data accuracy requirements, and the database system being used. The best technique often depends on the specific use case and the capabilities of the database system in use. I will explain more about HWM CDC in the next story.