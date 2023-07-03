# youtub-data-engineering-with-aws
## Overview
implemented a shell script that creates a pipeline to move the data to AWS S3. Subsequently, used AWS Lambda and Glue to perform transformations on the data, and stored it in a cleansed layer. Finally, analyzed the data using AWS QuickSight.  
## Dataset Trending YouTube Video Statistics
This Kaggle dataset contains statistics (CSV files) on popular daily YouTube videos over the course of many months. There are up to 200 trending videos published every day for many locations. The data for each region is in its own file. The video title, channel title, publication time, tags, views, likes and dislikes, description, and comment count are among the items included in the data. A category_id field, which differs by area, is also included in the JSON file linked to the region.

Find more about the dataset [Trending YouTube Video Statistics](https://www.kaggle.com/datasets/datasnaek/youtube-new)

 ## Tools and services used:
 - __Amazon S3__:  Amazon S3 is an object storage service that provides manufacturing scalability, data availability, security, and performance.
  - It is used as the staging layer for our raw data
  - Data Lake for raw, cleansed, and analytical data files
 - __AWS Glue__: A serverless data integration service that makes it easy to discover, prepare, and combine data for analytics
  - Used as the Data integration tool for our project.
  - Discover and build our raw, cleansed, and analytical metadata.
  - Create a Catalog for our data lake so we can easily query our data using AWS Athena.
-  __AWS Athena__: Athena is an interactive query service for S3 in which there is no need to load data it stays in S3.
  - Query our data from the data lake
  - Put a structure over our data lake to query our data easily and in an efficient way.
-  __AWS Lambda__: Lambda is a computing service that allows programmers to run code without creating or managing servers.
   - Extract, Transform our data files after they land in our raw data area.
   -  Make the ETL process automated using lambda triggers.
   - configure it to load the data from the raw area, clean it, and move it to the cleansed data area in our data lake.
- __QuickSight__: Serve as our BI tool to build our reports.
  - Connect to AWS Athena to load the data from our analytical storage area to build our reports.
  - Provide a secure connection, and automated reporting to enhance the decision-making process.
- __AWS IAM__: Identity and access management which enables us to manage access to AWS services and resources securely.
  - Define different roles for different users.
  - Allow managing data governance and Access management of different layers in our AWS S3 storage.
