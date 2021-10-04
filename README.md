# Associates Management System

## Description

This is Our Project Which is created in hive (Data Warehouse software, built in top of Hadoop). Which create and maintain the database of all associates trainings of various courses. In this Project we performed many different – different operations like table join, updating, creating etc, these operations are done on tables, we have 4 tables in this project.
Also we perform many various queries on these tables, we have 2 CSV data-sets, which are very useful for data loading, using queries we extract the data.

## Tools and Technologies
Hive

HDFS

SQL

Sqoop

MySQL


## Features


Effective Discount on every course.

Installment payment for Economically Weaker Section people.

Reschedule facility for Demo Missed and Demo Not Done Associates.

There are many courses.

Joining and Demo available Weekdays as well as WEEKENDS.

Fees Due data facility available if student forgot the data.

Update all records from Master Table using ORC.

Create another Data Set for Payment table because it has more features …


framework - Hive

Env - GCP

Files - .CSV, Docs, pptx

mode - lfs and cluster

data set - 2

file types - textfile, ORC file

property - ACID

data sets - master_table, payment table

table name - student_detail (master table )
              
              demo_table
              
              enrolled 
              
              payment 
 
 
 # All Steps - 
 

1 - load the data from local machine to GCP.

2 - go to inside hive using command ( HIVE )

3 - create a database

4 - use this database

5 - create a table temp table in textfile format ( master_table ) 

6 - load the data inside this temp table

7 - create a master table in ORC format

8 - load the data from temp table to master ORC table.

9 - create demo_table in ORC format

10 - load the data from master table to demo_table

11 - create enrolled table in ORC format

12 - load the data from master_table to enrolled table.

13 - create an another table for payment details in temp

14 - load the data from payment data set to payment temp table

15 - create a table for payment in ORC format.

16 - load the data from temp table to payment table.

17 - print all the data

18 - do various operation like insert data, update data and delete data.
