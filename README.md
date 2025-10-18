# Sales History ETL for Data Lake

This project implements a traditional ETL (batch) pipeline using Python and AWS services.
It simulates a real-world scenario where a company needs to process its daily sales data and store it in a Data Lake (Amazon S3) for further analysis with Amazon Athena.


# Objective

Extract historical sales data from a Kaggle CSV file, perform basic transformations using Python (pandas), and store the results in Amazon S3 in Parquet format, enabling efficient querying with Amazon Athena.


# Technologies Used

| Category    | Tool                                       |
| ----------- | ------------------------------------------ |
| Language    |    **Python** (pandas, boto3, awswrangler) |
| Storage     |    **Amazon S3**                           |
| SQL Query   |    **Amazon Athena**                       |
| Credentials |    **AWS IAM**                             |
| Development |    **Google Colab**                        |


# ETL Pipeline Structure

1 - Extraction

• Dataset: USA Online Shopping (Kaggle)

• Source file: .csv

• Data read and processed in Google Colab

2 - Transformation

• Column renaming and standardization

• Data type conversions

• Basic data cleaning and normalization

3 - Load

• Data saved in Parquet format

• Uploaded to S3 bucket: s3://data-engineer-projects-jota/projeto1/historico_compras.parquet


# Querying with Amazon Athena

• Created an external table in Athena based on the data stored in S3

• Executed SQL queries directly from Google Colab using awswrangler


# Results

• Transformed data stored in Parquet format
• Data available in Amazon S3 for analysis
• Table successfully created and queried in Amazon Athena
• Pipeline replicable, scalable, and ready for automation (via AWS Lambda in future iterations)


# Key Learnings

• Secure AWS connection setup using boto3 and awswrangler
• Data transformation best practices with pandas
• Efficient and structured storage in AWS Data Lake (S3)
• Analytical data querying using SQL on Amazon Athena
