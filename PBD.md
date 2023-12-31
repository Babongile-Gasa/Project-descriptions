Processing Big Data

The goal of this project was to ingest, profile, and test a historical stock market dataset to ensure it meets quality standards for use in developing automated trading algorithms. 

I downloaded the dataset containing daily pricing data for Nasdaq-traded companies from 1962-2021 from an S3 bucket. As a first subset, I ingested and converted the 1962 data into Parquet format. 
Next, I performed exploratory data analysis to derive statistics capturing data quality across completeness, validity, accuracy, consistency, uniformity, and uniqueness dimensions. Several data issues were identified and corrected.

To ensure thorough data quality across the Nasdaq stock dataset, I examined and addressed each of the six core dimensions:

1. Completeness - I checked for null values and missing data points in the time series. Where gaps existed, I interpolated values.
2. Validity - I plotted distributions of each feature to catch outliers. I capped anomalous values to within expected ranges based on domain knowledge.
3. Accuracy - I spot checked values against external sources. As no accuracy issues surfaced, no transformations were needed.
4. Consistency - I formatted date columns to a common timestamp format. I also made sure symbol naming conventions were consistent.  
5. Uniformity - I profiled summary statistics for each feature and made sure measures like means and spreads were aligned across individual stock tickers.
6. Conformity - I ensured features matched the specified data types and ranges required by our target systems. Any non-conforming elements were reformatted.

Finally, I automated ongoing data quality monitoring by implementing the Deequ library to regularly test new batches of trading data. Custom constraints were defined to check for missing values, outliers, and statistical thresholds indicating potential errors.

![DataQuality](https://github.com/Babongile-Gasa/Project-descriptions/assets/124687095/076cc2c1-8f44-4fbb-b31c-b97a004a86a3)

In summary, this project produced a reusable workflow for ingesting, transforming, and vetting Nasdaq ticker data both manually and automatically before use in financial models. Ensuring quality training data is vital for developing effective trading algorithms. The process is readily generalizable to other time series datasets as well.
