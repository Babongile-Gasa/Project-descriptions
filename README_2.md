Moving Big Data

The goal of this project was to develop a robust data pipeline for migrating historical stock market data from an on-premise system to the AWS cloud. The pipeline extracts data from 1000 CSV files, transforms it into a consolidated format, and loads it into a PostgreSQL database within Amazon RDS.

The pipeline was built using Airflow and runs on an Amazon EC2 instance. It leverages various AWS services including S3 for storage, RDS for the database, and SNS for notifications. The raw CSV data is processed using a Python script before loading into the target database tables that I configured. 
To enable automation, the pipeline is triggered by an event-driven AWS Lambda function which activates whenever new files are added to a monitored S3 bucket. Email alerts provide notifications on the success or failure of pipeline runs.
