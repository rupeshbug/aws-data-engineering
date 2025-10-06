## AWS Data Engineering

This repository contains CloudFormation templates and AWS resource configurations created while practicing AWS data engineering and infrastructure concepts. The YAML files define and deploy foundational cloud components such as VPCs, subnets, routing tables, security groups, and S3 buckets — all essential for building secure and scalable data workflows.

### ⚙️ Setup

The set-code.yaml file provisions the base networking and storage setup using AWS CloudFormation.

When executed, it automatically creates the following resources:

* VPC (Virtual Private Cloud)
* Two public subnets
* Security groups for network access control
* Routing table for managing traffic
* S3 bucket for data storage and processing


Before running the stack, specify a globally unique name for your S3 bucket. It is important for it to be globally unique so make sure to make it a bit long and add random numbers.


After the stack is deployed, complete these steps manually from the AWS Management Console:



1. Open the newly created S3 bucket.

2. Create the following folders inside it:

* rawData/
* processedData/
* scriptLocation/
* tmpDir/
* athena/


3. Upload source data into the rawData/ folder, maintaining the folder structure for:

* customers/
* employees/
* orders/

### 🧰 AWS Services Used

This project explores a range of AWS data services commonly used in real-world data engineering workflows, including:

* AWS Glue – for discovering, preparing, and transforming data for analytics and machine learning.
* AWS Glue ETL – to create and schedule extract-transform-load (ETL) jobs.
* Amazon Athena – for serverless querying and analysis of data stored in S3 using SQL.
* Amazon Redshift – for scalable data warehousing and analytics.
* Amazon Kinesis – for processing and analyzing streaming data in real time.
