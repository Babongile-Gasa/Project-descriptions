Storing Big Data Part 2 

The goal of this project was to develop a streaming data pipeline using AWS services to simulate an IoT sensor data feed. The pipeline collects simulated streaming data, transfers it to cloud storage, and provides monitoring capabilities. 

To accomplish this, I configured an AWS Lambda function to generate mock ticker data by reading and updating values in a DynamoDB table. This Lambda was set to execute every 60 seconds using a CloudWatch trigger. The streaming data output by the Lambda was then delivered to an Amazon Kinesis Data Firehose delivery stream which transported the data to an S3 bucket that I provisioned. I enabled public read access on this bucket to allow sharing of the streaming data.
For observability, I implemented a second Lambda that would notify me via email using Amazon SNS if failures occurred in the streaming Lambda. The streaming Lambda was configured to invoke this notification Lambda in case of errors. 
In the end, I had a fully automated pipeline ingesting simulated streaming data that I could visualize in the S3 bucket. The email alerts also validated that my monitoring solution was working to detect issues with the data flow. 

This project gave me hands-on experience with multiple AWS services including Lambda, DynamoDB, CloudWatch, SNS, Kinesis Firehose, and S3 to develop a serverless streaming application. The same principles and technologies could be applied to real-world IoT data streams.
