# Snowflake-END-to-END-ETL

![Group 2](https://github.com/saif-byte/Snowflake-END-to-END-ETL/assets/58662790/e24527ae-18d5-4aa5-b498-49f672e8d8b6)

Skills Used : AWS s3 buckets, AWS IAM , Snowflake Databases, Schemas , Tables , Pipes , Streams, Tasks, Snowflake compute , Snowflake Storage, snowcli

Hi, This is My Snowflake end to end ETL project. 

In this project , I have taken data from dataset uploaded on Kaggle named as 2015 Flight Delays and Cancellations. The dataset contains three csv files i.e flights, airlines & airports

I have uploaded the data to Amazon S3 Bucket. The S3 bucket structure is as follows:

s3://Flights Dataset/

│

├── flights_data/

│ └── flights.csv

│

├── airlines_data/

│ └── airlines.csv

│

├── airport_data/

| └── airports.csv

I then created amazon S3 integration in snowflake and made an external stage for all three tables folders.

Then  a pipe object is created to fetch data from respective s3 folders automatically whenever new data with certain file format is being uploaded.

Once we have data in external stage , it gets copied into landing database tables

after that a stream object is created that monitors the landing databases tables and capture if new information is being uploaded,

I then created new tasks that are scheduled to check if there is new data in stream and if there is it will copy that data into curated database tables by transforming it into required format.

from where it can be consumed for multiple uses such as ML , Reporting & Dashboarding etc.

Thanks 

