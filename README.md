# Data Modeling with Postgres Project
The goal of this project is to implement a star schema for analytic reason using Postgres and Python. This project is part of the Data Engineering Udacity Nano degree. 

# Data
There are two databases:
## Song Dataset: 
A subset of dara from <homepage xlink:type="simple" xlink:href="http://millionsongdataset.com/">Million Song Dataset</homepage>. the files are in JSON format.  
## Log Dataset:
The dara from <homepage xlink:type="simple" xlink:href="https://github.com/Interana/eventsim"> event simulator</homepage> based on the songs in the dataset above. These simulate activity logs from a music streaming app based on specified configurations.The files are also in JSON format. 

# Working Files:
## create_tables.py
this file used in creating and dropping the data. Run this file to reset the tables. (use it each time before running the ETL scripts)

## sql_queries.py
It contains all the SQL queries.

## etl.ipynb
read and process a single file from `song_data` and `log_data` and loads them into the tables. It explains the implementation process.

## test.ipynb
Display the first few rows of each table to let you check your database.

## etl.py
Read and process files from `song_data` and `log_data` and loads them into the tables.

# Result talbes
## Fact Table:
Table name: songplays 
Columns: songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent

## Dimension Tables
Table name: users
Columns: user_id, first_name, last_name, gender, level
Table name: songs
Columns: song_id, title, artist_id, year, duration
Table name: artists
Columns: artist_id, name, location, latitude, longitude
Table name: time
Columns: start_time, hour, day, week, month, year, weekday