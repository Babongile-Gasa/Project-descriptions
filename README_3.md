Processing Big Data

The goal of this project was to ingest, profile, and test a historical stock market dataset to ensure it meets quality standards for use in developing automated trading algorithms. 

I downloaded the dataset containing daily pricing data for Nasdaq-traded companies from 1962-2021 from an S3 bucket. As a first subset, I ingested and converted the 1962 data into Parquet format. 
Next, I performed exploratory data analysis to derive statistics capturing data quality across completeness, validity, accuracy, consistency, uniformity, and uniqueness dimensions. Several data issues were identified and corrected.
Finally, I automated ongoing data quality monitoring by implementing the Deequ library to regularly test new batches of trading data. Custom constraints were defined to check for missing values, outliers, and statistical thresholds indicating potential errors.

The workflow developed enables my team to identify and resolve data quality issues as part of an automated ingestion pipeline. By front-loading this process, higher quality training data can be reliably supplied to downstream trading algorithm development.


