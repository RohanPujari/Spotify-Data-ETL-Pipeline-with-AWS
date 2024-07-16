# Spotify-Data-ETL-Pipeline-with-AWS

## Project Overview:

This project demonstrates an end-to-end ETL (Extract, Transform, Load) pipeline for Spotify data using various AWS services. The pipeline extracts data from Kaggle, processes it using AWS Glue, and makes it available for analysis through AWS Athena and visualization with Amazon QuickSight.

## Architecture:

![image](https://github.com/user-attachments/assets/9e508014-3206-4446-a5a6-51068d5a3651)

## Components:

  - Data Source: Kaggle dataset containing Spotify data (artists, tracks, albums).

  - AWS S3: Two buckets - 'staging' for raw data and 'datawarehouse' for processed data.

  - AWS IAM: User and role creation with specific policies for Glue operations

  - AWS Glue: ETL job for data transformation

  - AWS Glue Crawler: For schema inference and table creation

  - AWS Athena: For querying transformed data

  - Amazon QuickSight: For data visualization

## Workflow:

1) Data Ingestion:
    - Downloaded Spotify dataset from Kaggle
    - Uploaded data to the 'staging' S3 bucket
2) IAM Setup:
    - Created an IAM user with specific access permissions
    - Set up an IAM role with necessary policies for Glue operations
3) ETL Process:
Developed a Glue ETL job to:
    - Extract data from the staging bucket.
    - Join and transform datasets.
    - Remove unnecessary columns.
    - Load transformed data into the 'datawarehouse' bucket as Parquet files.
4) Data Cataloging:
    - Used Glue Crawler to automatically infer schema and create table definitions.
    - Created a dedicated database to house the transformed data tables.
5) Data Analysis:
    - Utilized Amazon Athena for SQL-based querying of the transformed data.
    - Data Visualization:
    - Integrated Amazon QuickSight to create interactive dashboards.
6) Data Visualization:
    - Integrated Amazon QuickSight to create interactive dashboards.

## Difficulties Faced:
   - Errors caused due to incomplete policies given.
