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

## Content

table name - student_detail (master table )
              
              demo_table
              
              enrolled 
              
              payment 


## Features


Effective Discount on every course.

Installment payment for Economically Weaker Section people.

Reschedule facility for Demo Missed and Demo Not Done Associates.

There are many courses.

Joining and Demo available Weekdays as well as WEEKENDS.

Fees Due data facility available if student forgot the data.

Update all records from Master Table using ORC.

Create another Data Set for Payment table because it has more features …
 
 
 # Getting Started 
 

1 - create, use and show a database

              create database projectdb;
              
              show databases;
              
              use projectdb;
              


2 - create a table temp table in textfile format ( master_table ) and load the data.

              create table temp(id int, name string, mail string, mobile string, course string, age int, gender string, fee int, discount string, status1 string, status2 string)row format delimited fields terminated by ',' stored as textfile;

              laod data local inpath '/home/piyushji2000/Main_table1.csv/' into table temp;



3 - create a master table in ORC format and load data from temp tp ORC

              create table Student_details(id int, name string, mail string, mobile string, course string, age int, gender string, fee int, discount string, status1 string, status2 string)stored as orc tblproperties('transactional'='true');

              insert into Student_details select * from temp;


4 - create demo_table in ORC format

              create table demo_table(id int, name string, mail string, contact string, course string, demo_status1 string, demo_status2 string)stored as orc tblproperties('transactional'='true');

              insert into demo_table select id,name,mail,mobile,course,status1,status2 from Student_details where status1='DS' or status1='DM' or status1 = 'DD';


5. create enrolled table and load the data

              create table enrolled(id int, name string, mail string, contact string, course string, enroll_status1 string, enroll_status2 string)stored as orc tblproperties('transactional'='true');

              insert into enrolled select id,name,mail,mobile,course,status1,status2 from Student_details where status1='J';

6 - create an another table for payment details in temp and load data.

               create table temp1(id int, name string, mail string, mobile string, course string, fee int, discount string, total_fee int, no_of_installment int, mode_of_payment string, deposite_fee int, remaining_fee int, fee_deposite_date string, due_date string) row format delimited fields terminated by ',' stored as textfile;

               load data local inpath '/home/piyushji2000/payment_details.csv/' into table temp1;


7. update record 

               insert into student_details values(101,‘Piyush',‘Piyush@gmail.com','458-965','SQL',24,'M',25000,'15%','DD','WD-WED-11AM'),(102,'aysha','aysha@gmail.com','125-632','ML',21,'F',20000,'20%','J','WED-10AM');

                insert into demo_table select id,name,mail,mobile,course,status1,status2 from student_details where id=101;

                insert into demo_table select id,name,mail,mobile,course,status1,status2 from student_details where id=101;

                update student_details set status1='J' where id=101;

                delete from demo_table where id=101;

                
## Keynotes

Make this more flexible.

Will Integrate with UI.

Grab the data in real time scenario.

Secure all DB at Admin Panel

Try to make a  web app and integrate with this DB.

Deploy this project on AWS( For Faster Response ).

Provide some referral cash back for each & every Associates.


## Contributors

Piyush Goyal

Aysha Muktesar

Surya Dev Gedela

Bhawana Priya
