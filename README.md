# Spotify End-To-End Data Pipline

### Description
In this project, we will build an ETL(Extract, Transform, Load) pipeline using Spotify API on AWS. The pipeline will retrieve the data from Spotify API, transform it to a desired format, and load it into an AWS data store.

### Architecture
![Architecture Diagram](https://github.com/nishant0201/spotify-data-pipeline/blob/main/Spotify_Data_Pipeline.jpg)

### About Dataset/API
This API contains information about music artist, albums and songs - [Spotify API](https://developer.spotify.com/documentation/)

### Services Used
1. **S3 (Simple Storage Service):** Amazon S3(Simple Storage Service) is a highly scalable object storage service that can store and retrieve any amount of data from anywhere on the web. It is commonly used to store and distribute large media files, data backups, and static website files.

2. **AWS Lambda:** AWS Lambda is aserverless computing service that lets you run your code without managing servers. You can use Lambda to run code in response to events like changes in S3, DynamoDb, or other AWS Services.

3. **Cloud Watch:** Amazon Cloudwatch is a monitoring service for AWS resources and the application you run on them. You can use Cloudwatch to collect and track metrics, collect monitor log files, and set alerts.

4. **Glue Crawler:** AWS Glue Crawler is a fully managed service that automatically crawl your data sources, identifies data formats, and infers schemas to create an AWS Glue Dta Catalog.

5. **Data Catalog:** AWS Glue Data Catalog is a fully managed metadata repository that makes it easyto discover and manage data in AWS. You can use the Glue Data Catalog with other AWS services, such as Athena.

6. **Amazon Athena:** Amazon Athena is an interactive query service that makes it easy to analyze data in Amazon S3 using standard SQL. You can use Athena to analyze data in your Glue Data Catalog or in other S3 buckets.

### Project Execution Flow
Extract Data from API -> Lambda Trigger (every 1 hour) -> Run Extract Code -> Store Raw Data -> Trigger Transform Function -> Transform Data and Load It -> Query Using Athena
