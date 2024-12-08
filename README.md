# Spotify Data ETL Pipeline using AWS  

This project demonstrates an **ETL (Extract, Transform, Load)** pipeline that fetches Spotify data using their API and processes it using AWS services like Lambda, S3, Glue, and Athena. The pipeline is designed to extract raw data from Spotify, transform it into a structured format, and load it into a queryable state for analytics.

---

## **Project Workflow**  

1. **Extract**:
   - Data is fetched from the Spotify API using Python and a Lambda function triggered by **CloudWatch**.  
   - The raw JSON data is stored in an S3 bucket.  

2. **Transform**:
   - A second AWS Lambda function processes the raw data.  
   - It transforms the data into a tabular or CSV format and saves the output to an S3 bucket.  

3. **Load**:
   - **AWS Glue Crawler** infers the schema of the transformed data and updates the **Glue Data Catalog**.  
   - The data is made queryable in **Amazon Athena** for analytics and reporting.  

---

## **Architecture Diagram**
![Architecture-diagram](https://github.com/user-attachments/assets/b6a1885a-e0db-4d94-a330-dded574c238a)



---

## **Technologies Used**
- **Spotify API**: To fetch playlists and music-related data.  
- **Python**: For extraction and transformation.  
- **Amazon CloudWatch**: For triggering the pipeline.  
- **AWS Lambda**: Serverless computing for data processing.  
- **Amazon S3**: Storage for raw and transformed data.  
- **AWS Glue**: Schema inference and data cataloging.  
- **Amazon Athena**: Querying transformed data for insights.  

---

## **Features**  
- Automated data extraction using CloudWatch triggers.  
- Serverless transformation of raw Spotify data into clean, structured formats.  
- Queryable data using Athena for easy analytics and reporting.  
