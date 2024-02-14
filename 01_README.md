**Spotify_E2E_ETL_DataEngineering_project -**
Project focuses on constructing a robust ETL (Extract, Transform, Load) pipeline utilizing the Spotify API within the AWS environment. The pipeline seamlessly extracts data from the Spotify API, undergoes transformation processes to achieve the desired format, and efficiently loads it into a designated AWS data store. This initiative harmonizes the power of Spotify's API with the scalability and reliability of AWS, showcasing our commitment to streamlined data processing and storage.

**Architecture Diagram**

![image](https://github.com/sudarshanp1/Spotify_E2E_ETL_DataEngineering_project/assets/121892659/e3bce2ae-3fc1-45f6-a635-b04e84b2d3b8)

The Spotify API encompasses comprehensive data on music artists, albums, and songs. - [Spotify API](https://developer.spotify.com/documentation/web-api)https://developer.spotify.com/documentation/web-api

**Services Used**

**S3** (Simple, Storage, Service): Amazon S3 (Simple Storage Service) is a highly scalable object storage service that can store and retrieve any amount of data from anywhere on the web. It is commonly used to store and distribute large media files, data backups, and static website files.

**AWS Lambda:** AWS Lambda is a serverless computing service that lets you run your code without managing servers. You can use lambda to run the code in response to events like changes in S3, DynamoDB, or other Amazon Web Services.


**CloudWatch:** Amazon CloudWatch is a monitoring service for AWS resources and the applications you run on them. You can use ClooudWatch to collect and track metrics, collect and monitor log files, and set alarms.


**Glue Crawler:** AWS Glue Crawler is a fully managed service that automatically crawls your data sources, identifies the data format, and infers schemas to create an AWS Glue Data Catalog.


**Data Catalog:** AWS Glue Data Catalog is a fully managed service that automatically crawls your data sources, identifies the data formats, and infers schemas to create an AWS Glue Data Catalog with other Amazon Web Services, such as Athena.


**Amazon Athena:** Amazon Athena is an Interactive query service that makes it easy to analyze data in Amazon S3 using standard SQL. You can use Athena to analyze data in your Gllue Catalog or other S3 Buckets.

**Lambda, AWS & Loading**

Extract Data from API -> Lambda Trigger (Every 1 Hour) -> Run extract Code -> Store Raw Data -> Trigger Transformation Function -> Transform Data and Load it -> Query using Athena.
Data Extraction(request data) from Spotify API triggers Lambd--> executing extraction code-->Raw data is stored in S3--> initiating transformation (through a pythonic process) and loading via Lambda-->Resulting data is queryable through Athena(creating own data lake), facilitating dynamic exploration.
