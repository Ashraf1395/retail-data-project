# retail-data-project

Export data from mysql-database to REDSHIFT using pyspark

Problem Statement:
We need to build an ETL pipeline to dump mysql data base record to redshift by doing necessary transformations using spark 
so that we can perform analytical queries to create Analysis reports,dashboards and Machine Learning Models for predictions.

We will design Star Schema so that we can export above attached OLTP to OLAP

OLTP Design
![MY SQL DATABASE](./mysql-oltp-database.png)

RedShift Dataware house(OLAP Design)
![Red Shift](./redshift-olap-diagram.png)

Approach
1. Read data from mysql using pyspark and perform transformations to create OLAP from OLTP and then dump it in S3 bucket

2. Read data from s3 bucket and dump in REDSHIFT and perform Analytical Queries
![s3-redshift](./s3-redshift.png)

3. We can Create KPI Reports using this data,Sales Dashboards or build Machine Learning Models.
Launch entire server setup
```
