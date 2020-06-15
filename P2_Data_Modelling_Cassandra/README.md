Purpose
Here we are doing Data Modeling for a startup called "Sparkify". It is an online music streaming platform. The startup was collecting data on songs and user activity on the streaming platform. Here Data Modeling is done to empower the analytics team for getting tons of insights from the available data.

Datasets
Song Dataset - Complete details and metadata about the song
Log Dataset - User activity log

Database Schema
Here we are using "Star Schema" to model this dataset by dividing them into facts and dimensions so that it is in a structured manner.

Fact Table
Fact table is going to be "songplays" table which contains the metadata of the complete information about each user activity. Many dimension tables are connected to one fact table.

Dimension Tables
Here "users","songs","artists","time" are going to be dimension tables. These tables will be having detailed information about a single row from facts table.

ETL Pipleline
I have created an ETL pipeline which collects data from the json log files and then inserts them into respective tables. "etl.py" file consists of the complete pipeline

Files Explained
There are 7 files in this project.

1. data - This folder contains the log and song datasets.
2. etl.ipynb - This is a jupyter notebook which I used to create the skeleton for the pipeline. It is kind of a workbook.
3. test.ipynb - This jupyter notebook checks whether the written scripts for creating tables and inserting data are working fine or not.
4. create_tables.py - This program contains postgresql queries for creating the database and tables.
5. etl.py - This script contains the complete ETL pipeline for the project.
6. Readme.md - Documentation regarding the project.
7. sql_queries.py - This python script contains the create and insert contains for the database.

How to run the project ?

To run the project, make sure you have all the above files at a single place.

Go to terminal and first run create_tables.py script by typing "python create_tables.py" in the terminal. This will make sure that all the previous databases are dropped and new database with tables are created.

Go ahead and run etl.py script by typing "python etl.py". This will run the etl pipeline and extract data from the log files and insert them into the facts and dimension table.s