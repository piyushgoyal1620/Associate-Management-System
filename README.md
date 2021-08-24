# Student-Project
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
