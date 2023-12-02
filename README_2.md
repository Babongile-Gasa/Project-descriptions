Moving Big Data

The goal of this project was to develop an automated data pipeline to ingest, process, and load on-premise stock market data into the AWS cloud. The pipeline extracts raw CSV files containing historical trading data for 1000 companies, transforms this into a consolidated dataset, and loads it into an Amazon RDS PostgreSQL database.

To enable this batch ETL process, I configured underlying AWS services including Amazon S3 for storage, EC2 for processing, RDS for the database, and SNS for notifications. These components were orchestrated into an event-driven Airflow workflow running in Docker on the EC2 node.
The pipeline is triggered via an object upload to an S3 bucket monitored by a Lambda function. On invocation, Airflow performs the data transformations in Python and uses pgAdmin to populate the PostgreSQL data tables. Email alerts inform of success or failure.

In summary, this project demonstrated proficiency in designing modular data pipelines leveraging cloud services. The serverless architecture minimizes overhead while enabling scalability. Automating the workflow through event triggers ensures new data will load without manual intervention. 

![end-to-end-pipeline](https://github.com/Babongile-Gasa/Project-descriptions/assets/124687095/74dad609-296d-4237-9b5c-5b3524ffac6d)

