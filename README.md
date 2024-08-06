# Coffee shop data pipeline with hadoop

## Overview

This project is part of the **Road to Data Engineer Special Live**. The goal of this project is to created pipeline for both data from csv file and streaming data.

![project architect](hadoop.PNG)
The diagram depicts a Hadoop system architecture designed for handling both batch and real-time data processing. It outlines two primary layers:

- **Batch Layer**: Processes large volumes of historical data in batches for analysis and reporting.
- **Speed Layer**: Handles real-time data streams for immediate insights and updates.

## Batch Layer Workflow

### Data Ingestion

- **Source System**: Text files are generated in form of csv.
- **CLI**: The Hadoop command-line interface (CLI) is used to interact with the system.
- **HDFS**: Text files is stored in the Hadoop Distributed File System (HDFS).

### Data Processing

- **SparkSQL**: Data is loaded into SparkSQL for data cleansing.
- **HIVE**: Data is transformed and queried using Hive which is a data warehousing infrastructure built on top of Hadoop.

### Output

- **Tables**: Processed data is stored in Hive tables for further analysis or reporting.

## Speed Layer Workflow

### Data Ingestion

- **Source System**: Log files are generated from a source system.
- **Flume**: Flume is used to collect, aggregate, and move log data into the Hadoop ecosystem.
- **HDFS**: Log data is stored in HDFS.
- **HBASE**: Data is stored in HBase, a NoSQL database optimized for fast read/write operations.

### Data Processing

- **Spark Streaming**: Real-time data is processed using Spark Streaming.
- **HIVE**: Data is transformed and queried using Hive.


### Output

- **Tables**: Processed data is stored in Hive tables for further analysis or reporting.

## Key Components

- **HDFS**: Provides distributed storage for both batch and real-time data.
- **Spark**: A unified analytics engine for batch and streaming data processing.
- **Hive**: A data warehousing infrastructure built on top of Hadoop for SQL-like queries.
- **Flume**: A distributed, fault-tolerant, and available system for efficiently collecting, aggregating, and moving large amounts of log data.
- **HBASE**: A NoSQL database optimized for fast read/write access, suitable for real-time applications.
