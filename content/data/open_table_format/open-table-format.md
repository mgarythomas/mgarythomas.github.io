---
title: "Open Table Format"
description: "An overview of the Open Table Format and why it is important."
draft: true
tags: ["open table format", "data"]
categories: ["data"]
author: "Gary Thomas"
date: 2025-05-15
---

## Introduction

The Open Table Format (OTF) is a data format that is used to store data in a tabular format. It is a simple and easy to use format that is designed to be human-readable and easy to parse. It is a text-based format that is based on the CSV (Comma Separated Values) format.

Open table formats are an open-source technology for storing tabular data that builds on top of existing file formats like Parquet and ORC. An open table format stores your tabular data in files and stores metadata (about your data and operations) in a separate file or directory. This metadata is used to enable many of the great features of open table formats: faster query speeds, more reliable transactions and lower risk of data corruption.

There are 3 main formats that meet this criteria:
1. [Apache Iceberg](https://iceberg.apache.org/)
2. [Delta Lake](https://delta.io/)
3. [Apache Hudi](https://hudi.apache.org/)

There is probably a good discussion as to whether Apache Hudi is losing that particular battle and market share/thought leadership to Delta Lake and Apache Iceberg. 

While there are differences between the different open table formats, these differences are becoming less important as technologies emerge to support interoperability. Projects like Delta Lake UniForm and Unity Catalog are bridging the gap between open table formats.

## Key Features

### ACID Compliance

ACID (Atomicity, Consistency, Isolation, Durability) is a set of properties that ensure the integrity of data in a database. ACID compliance is important for ensuring that data is consistent and reliable, and that transactions are completed successfully.

### Schema Enforcement and Evolution

Schema evolution is the ability to change the schema of a table without affecting the existing data. This is important for ensuring that the data warehouse can adapt to changing business needs and requirements.

### Advanced Data Skipping

Data skipping is the ability to skip data that is not relevant to a query. This is important for ensuring that queries are fast and efficient.

### Time Travel

Time travel is the ability to query historical data in a data warehouse. This is important for ensuring that the data warehouse can provide insights into past events and trends.

### CRUD Operations

CRUD (Create, Read, Update, Delete) operations are the basic operations that are performed on data. These operations are important for ensuring that data is consistent and reliable, and that transactions are completed successfully.




