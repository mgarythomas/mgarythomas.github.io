---
title: "Why Parquet?"
summary: "Parquet is a columnar storage format that offers advantages for big data processing and analytics"
description: "Parquet is a columnar storage format that is optimized for analytics and provides a scalable, cost-effective, and flexible solution for data analytics. Why is it important?"
draft: false
tags: ["parquet", "data warehouse","columnar", "storage", "big data", "data analytics"]
categories: ["data"]
author: "Gary Thomas"
image: "/data/why_parquet/parquetFileStructure.svg"
url: "/data/parquet/"
date: 2025-04-30
---

## Introduction

[Parquet](https://parquet.apache.org/) is a columnar storage format that is optimized for analytics and provides a scalable, cost-effective, and flexible solution for big data processing and for data analytics. Why is it important?
 It is designed for efficient data storage and retrieval. It provides high performance compression and encoding schemes to handle complex data in bulk and is supported in many programming language and analytics tools.

 It was developed by Twitter and [Cloudera](https://www.cloudera.com/) to provide an efficient columnar representation of data for projects within the Hadoop ecosystem. It was first released in 2012 and has since become a de-facto standard for big data processing and analytics.

## Key features of Parquet

### Columnar Storage

Parquet is a columnar storage format that stores data in columns, which can be read and written in parallel. This allows for faster data processing and analysis, as well as the ability to query specific columns of data without having to read the entire dataset.
It could also be described as a **hybrid-based** storage format, as it stores data in both row and column formats (rows are grouped by row groups and then column partitioned)

### Self-Describing

Parquet stores the structure of the data in the file, which allows for easy reading and writing of the data without the need for a schema

### Binary Format

Parquet is a binary format, which allows for efficient storage and retrieval of data.

### Compression and Encoding

Parquet is built to support very efficient compression and encoding schemes. Multiple projects have demonstrated the performance impact of applying the right compression and encoding scheme to the data. Parquet allows compression schemes to be specified on a per-column level, and is future-proofed to allow adding more encodings as they are invented and implemented.

Parquet supports various compression algorithms, including Snappy, LZO, Gzip, and LZ4. The choice of compression algorithm depends on the specific characteristics of the data and the requirements of the analytical workloads. In addition to compression, Parquet also supports several encoding techniques, such as dictionary encoding, run-length encoding, and delta encoding. These encoding techniques can further improve storage efficiency and query performance.

### Splitable

Parquet files are splittable, enabling efficient parallel processing of large files and faster data loading and querying. This is because Parquet files can be divided into smaller chunks, each of which can be processed independently by multiple processors or nodes in a distributed system. This capability is crucial for large-scale data processing and analytics, as it enables faster data loading and querying by leveraging parallel computing.

### Rich Data Structure

Parquet was developed to support nested data structures from the beginning. This support for [string and assembly algorithms](https://github.com/julienledem/redelm/wiki/The-striping-and-assembly-algorithms-from-the-Dremel-paper) allows for efficient storage and retrieval of data. For further background, see the [Dremel paper](https://research.google/pubs/dremel-a-decade-of-interactive-sql-analysis-at-web-scale/).

## Structure

![Parquet Structure](/data/why_parquet/parquetFileStructure.svg)

The Parquet file layout is composed of a header, footer, and data block, with the header containing information about the file format, and the footer containing metadata such as statistics and schema information. The data block is divided into row groups, which are further divided into columns, and the values within each column are stored as pages. This layout allows for efficient compression and encoding, which reduces storage space and improves read performance.

A Parquet file is made up of a number of components:

- File Header (Each file begins with a magic number to identify the parquet file)
- Row Group (A logical horizontal partitioning of the data into rows)
- Column Chunk (Chunks of the data grouped by column)
- Page (Column chunks are further divided into pages, which are the smallest units of storage and compression.) Every Page has:
    - Page Header (Contains the page type, number of values, and other metadata)
    - Page Data (The actual column values which are typically compressed and encoded)
- File Metadata (which is made up of a number of distinct items of data, such as the schema, row groups, and column chunks)
    - Schema definition
    - Row Group Metadata
    - Column Metadata (The location of all the column metadata start locations)
    - Statistics (Summary statistics for each column, such as min, max, and null count)
