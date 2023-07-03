# youtub-data-engineering-with-aws
## Overview
implemented a shell script that creates a pipeline to move the data to AWS S3. Subsequently, used AWS Lambda and Glue to perform transformations on the data, and stored it in a cleansed layer. Finally, analyzed the data using AWS QuickSight.  
## Dataset Trending YouTube Video Statistics
This Kaggle dataset contains statistics (CSV files) on popular daily YouTube videos over the course of many months. There are up to 200 trending videos published every day for many locations. The data for each region is in its own file. The video title, channel title, publication time, tags, views, likes and dislikes, description, and comment count are among the items included in the data. A category_id field, which differs by area, is also included in the JSON file linked to the region.

Find more about the dataset [Trending YouTube Video Statistics](https://www.kaggle.com/datasets/datasnaek/youtube-new)

 ## Tools and services used:
 - __Amazon S3__: Amazon S3 is an object storage service that offers manufacturing scalability, data availability, security, and performance.
   - It serves as the staging layer for our raw data.
   - Acts as the data lake for raw, cleansed, and analytical data files
 - __AWS Glue__:AWS Glue is a serverless data integration service that simplifies the process of discovering, preparing, and combining data for analytics.
   - It functions as the data integration tool.
   - Enables the discovery and building of raw, cleansed, and analytical metadata.
   - Creates a catalog for our data lake, facilitating easy data querying with AWS Athena.
-  __AWS Athena__: Athena is an interactive query service for S3 that eliminates the need to load data, as it remains in S3.
   - It allows us to query our data directly from the data lake.
   - Provides a structured approach to querying our data lake in an efficient manner.
-  __AWS Lambda__: Lambda is a computing service that enables running code without the need to create or manage servers.
   -  It is utilized to extract and transform our data files once they land in the raw data area.
   -  Automates the ETL process using lambda triggers.
   - Configured to load, clean, and move data from the raw area to the cleansed data area in our data lake.
- __QuickSight__:  QuickSight serves as our business intelligence tool for report generation.
  - It connects to AWS Athena to fetch data from our analytical storage area for report building.
  - Provides secure connections and automated reporting, enhancing the decision-making process.
- __AWS IAM__: AWS IAM (Identity and Access Management) enables secure management of access to AWS services and resources.
  - It allows us to define different roles for various users.
  - Facilitates data governance and access management across different layers of our AWS S3 storage.
## Project life cycle


