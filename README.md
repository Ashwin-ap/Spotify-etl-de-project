# Spotify-ETL-DE-Project

### Description
In this project, have built an ETL(Extract, Transform, Load) pipeline using the Spotify API on AWS. The pipeline will retrieve data from the spotify API, transform it to a desired format and load it into AWS S3 buckets.

### About Dataset/API
This API contains information about music artists, albums and songs - [Spotify API](https://developer.spotify.com/documentation/web-api)

### Services Used
1. **S3 (Simple Storage Service):** It can store and retrieve data from anywhere on the web.
   
2. **AWS Lambda:** AWS Lambda is a serverless computing service that lets you run your code without managing servers. It can run code in response to events like changes in S3, DynamoDB, or other AWS Services.
   
3. **Cloud Watch:** Amazon CloudWatch is a monitoring service for AWS resources and the applications that run on them.

4. **Glue Crawler:** It's designed to automate the process of discovering and cataloging metadata from various data sources.

5. **Data Catalog:** A data catalog is a centralized repository that stores and manages metadata information about various datasets within an organization.

6. **Amazon Athena:** It allows us to analyze data stored in Amazon S3 using standard SQL queries.

### Insyall Packages
```
pip install pandas
pip install numpy
pip install spotipy
```

### Project Execution Flow
Extract Data from API -> Lambda Trigger (every 1 hour) -> Run Extract Code -> Store Raw Data -> Trigger Transform Function -> Transform Data and Load it -> Query Using Athena   
