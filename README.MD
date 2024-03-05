# Stock Market Kafka Real-Time Data Engineering Project

## Introduction

In this project, I have implemented an End-To-End Data Engineering solution for processing real-time stock market data using Apache Kafka. This project leverages various technologies such as Python, Amazon Web Services (AWS), Apache Kafka, Glue, Athena, and SQL to ingest, process, and analyze the stock market data.

## Architecture

![Architecture Diagram](https://i.ibb.co/KDXqLkb/Architecture.jpg)

### Data Flow

1. Data is produced from a Stock Market App Simulation and an AWS Glue Crawler.
2. The produced data is then published to Kafka topics.
3. Amazon S3 and Amazon Athena, subscribed to the topics and consumed the data.
4. Amazon S3 stores the data for archival purposes, while Amazon Athena provides interactive querying capabilities for the data.

### Technology Used

- **Programming Language**: Python
- **Amazon Web Services (AWS)**:
  - **S3 (Simple Storage Service)**: Used for storing raw and processed data.
  - **Athena**: Allows querying data stored in S3 using standard SQL queries.
  - **Glue Crawler**: Automatically discovers the schema of data stored in S3 and updates the Glue Catalog.
  - **Glue Catalog**: A centralized metadata repository for data stored in S3.
  - **EC2**: Virtual servers used for running various data pipeline components.
- **Apache Kafka**: Distributed streaming platform used for collecting, processing, and distributing real-time data.

