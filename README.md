# NYC_TLC_Yellow_Taxi_MapReduce
NYC Yellow Taxi data analysis using Big Data tools such as Hadoop Framework, Apache HBase, Apache Sqoop, and AWS to solve business problems. The dataset from year 2017 includes trip records and related information.

# Dataset for the Analysis:
https://nyc-tlc-upgrad.s3.amazonaws.com/yellow_tripdata_2017-01.csv
https://nyc-tlc-upgrad.s3.amazonaws.com/yellow_tripdata_2017-02.csv
https://nyc-tlc-upgrad.s3.amazonaws.com/yellow_tripdata_2017-03.csv
https://nyc-tlc-upgrad.s3.amazonaws.com/yellow_tripdata_2017-04.csv
https://nyc-tlc-upgrad.s3.amazonaws.com/yellow_tripdata_2017-05.csv
https://nyc-tlc-upgrad.s3.amazonaws.com/yellow_tripdata_2017-06.csv

# Tasks:

## 1. Data Ingestion Task:
Task 1. Create an RDS instance in your AWS account and upload the data to the RDS instance.

Since the dataset is huge, you need to upload the data from only two files (i.e. yellow_tripdata_2017-01.csv & yellow_tripdata_2017-02.csv) from the dataset.

IMPORTANT NOTE: You will need to create an appropriate schema before uploading the data sets to AWS RDS (you can find the data dictionary attached here). The steps on how to create an AWS RDS instance can be found in the Additional content of the 'Introduction to Cloud Computing and AWS Setup' module and the steps to work with RDS in the link shared in the next segment)

Task 2. Use Sqoop command to ingest the data from RDS into the HBase Table.

Task 3. Bulk import data from next two files in the dataset on your EMR cluster to your HBase Table using the relevant codes.

Note: For the above task 3, you just need to import data from the subsequent 2 csv files (i.e. yellow_tripdata_2017-03.csv & yellow_tripdata_2017-04.csv) on your EMR cluster.

## 2. MapReduce Tasks:
Task 4. Write MapReduce codes to perform the tasks using the files you’ve downloaded on your EMR Instance:

1. Which vendors have the most trips, and what is the total revenue generated by that vendor?
2. Which pickup location generates the most revenue? 
3. What are the different payment types used by customers and their count? The final results should be in a sorted format.
4. What is the average trip time for different pickup locations?
5. Calculate the average tips to revenue ratio of the drivers for different pickup locations in sorted format.
6. How does revenue vary over time? Calculate the average trip revenue per month - analysing it by hour of the day (day vs night) and the day of the week (weekday vs weekend).

## 3. Optional Tasks:
Task 5. Use Sqoop export command to export the results of each MapReduce tasks above to your RDS instance. Use the RDS connection string connection to visualise the dataset using a dashboarding tool (Google Data Studio, Tableau or PowerBI)
