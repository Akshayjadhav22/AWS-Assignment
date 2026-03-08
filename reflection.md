# Reflection – SmartGear AWS Data Pipeline

1.While implementing the SmartGear pipeline using AWS services, the biggest surprise was how seamlessly serverless services integrate with each other. Amazon S3 served as the central storage layer for the entire pipeline, while AWS Glue handled ETL processing using Spark without requiring infrastructure management. Athena made it possible to query data directly from S3 using SQL without loading it into a traditional database.

2.One challenge I faced was configuring permissions and paths for the Glue job. Initially, the job failed due to incorrect S3 permissions and path configuration. After checking the IAM role permissions and correcting the S3 output location, the Glue job successfully processed the data and generated the Parquet files.

3.Glue is best suited for large-scale ETL processing where distributed data transformation is required. Athena is ideal for ad-hoc querying and quick analysis of data stored in S3 using SQL. An S3-only approach would be sufficient when data simply needs to be stored and accessed by applications without transformation or analytical querying.

