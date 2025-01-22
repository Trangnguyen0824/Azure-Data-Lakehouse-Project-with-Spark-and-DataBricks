# Azure-Data-Lakehouse-Project-with-Spark-and-DataBricks
Summary : Using Python, Spark and Azure Databricks to create a data lakehouse architecture.

## Introduction
Some of the data is from Divvy, a bike sharing program in Chicago, Illinois. This data is anonymous, so Udacity provided some fake rider and account profiles to go along with fake payment data.

A rider can purchase a pass at a kiosk or use a mobile application to unlock a bike at stations around the city and use the bike for a specified amount of time. The bikes can be resturned to the same station or to another station.

## Project Description
Using the Azure tech stack, I wanted to create the following architecture:

architecture diagram

In Azure, I uploaded csv files to the Databricks file system (DBFS).

The files were then moved from the DBFS to be stored as parquet files in the delta lake.

At this point, the files were moved to a bronze table storage in the delta lake.

Finally, the tables were cleaned and prepared for analysis by creating the dimension and fact tables below.

The transformations and creation of the tables were done via Python and Spark (sql)


## Analysis - Questions that now can be answered
### Analyze how much time is spent per ride:

Based on date and time factors such as day of week and time of day
Based on which station is the starting and / or ending station
Based on age of the rider at time of the ride
Based on whether the rider is a member or a casual rider
### Analyze how much money is spent:

Per month, quarter, year
Per member, based on the age of the rider at account start
### Analyze how much money is spent per member:

Based on how many rides the rider averages per month
Based on how many minutes the rider spends on a bike per month
