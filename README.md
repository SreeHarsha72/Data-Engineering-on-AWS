# Youtube Data Analysis on AWS

## Introduction
This repository details end-to-end data engineering project leveraging AWS services. The project simulates a real-world scenario where a client seeks to analyze YouTube ad campaigns and uncover factors affecting video popularity.

## Project Overview
- Scenario Assumption: The client wants to run YouTube ad campaigns and requires insights into video popularity trends.
- dataset https://www.kaggle.com/datasets/datasnaek/youtube-new

## Goals
+ Categorize videos based on comments and stylistics.
+	 Build a scalable data lake and ETL pipeline.
+	 Utilize AWS services such as S3, Glue, Lambda, and Athena.
+	 Develop a dashboard for actionable insights.

## AWS Services Used
+	 Amazon S3: Central repository for storing raw and processed data.
+	 AWS Lambda: Processes JSON data, handles ETL workflows, and automates triggers.
+	 AWS Glue: Crawlers create metadata catalogs, and ETL jobs transform raw data.
+	 AWS Athena: Enables SQL querying of transformed data for insights.
+	 AWS QuickSight: Visualizes trends and creates interactive dashboards.
+	 IAM (Identity Access Management): Ensures secure access to AWS resources.

## Data Preparation
### 1. Data Source:
+	 The dataset consists of trending YouTube videos and their categories, sourced from Kaggle.
### 2. Storage:
+	 Raw data is stored in Amazon S3 using structured naming conventions for easy access and organization.

## Work Steps
### 1. Data Lake Creation:
+	 AWS S3 serves as the central repository for raw and processed data.
### 2. 	Data Transformation:
+	 AWS Lambda functions process JSON data into a tabular format (Parquet) for optimized storage and querying.
+	 AWS Glue crawlers catalog metadata for structured querying.
### 3. Building Analytical and Reporting Layers:
  +  Transformed processed data into an analytical/reporting layer using AWS Glue Studio.
  + Partitioned data by region and category to enhance query performance.
### 4. Visualization with AWS QuickSight:
+	AWS QuickSight was used to create interactive dashboards and visualize trends, including:
    +	Most liked or viewed video categories.
    +	Regional insights into video performance.
+	 Steps included connecting QuickSight to Athena and designing user-friendly dashboards for stakeholders.

## Error Handling
+	 Nested JSON Challenges: Resolved through pre-processing steps before Glue ETL.
+	 Data Type Mismatches: Addressed by modifying Glue schemas and reprocessing data using Lambda.
+	 Timeout Issues in Lambda: Resolved by optimizing code and utilizing AWS Lambda layers for dependencies.



