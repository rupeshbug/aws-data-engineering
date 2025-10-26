## AWS Data Engineering

This repository contains CloudFormation templates and AWS resource configurations created while practicing AWS data engineering and infrastructure concepts. The YAML files define and deploy foundational cloud components such as VPCs, subnets, routing tables, security groups, and S3 buckets — all essential for building secure and scalable data workflows. It also contains folders which are projects in seperate folders and resources of it.

### ⚙️ Setup

The set-code.yaml file provisions the base networking and storage setup using AWS CloudFormation.

When executed, it automatically creates the following resources:

* VPC (Virtual Private Cloud)
* Two public subnets
* Security groups for network access control
* Routing table for managing traffic
* S3 bucket for data storage and processing


Before running the stack, specify a globally unique name for your S3 bucket.


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

* Amazon S3 – Data lake for raw and processed data.
* AWS Glue – Data discovery, transformation, and ETL jobs.
* AWS Lambda – Event-driven transformations.
* Amazon Athena – for serverless querying and analysis of data stored in S3 using SQL.
* Amazon Redshift – for scalable data warehousing and analytics.
* AWS CloudFormation – Infrastructure-as-code for repeatable environments.
