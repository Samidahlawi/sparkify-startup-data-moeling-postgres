# Project Overview.
    The Sparkify is startup want to analyze the data and they have been collecting on user activity and songs on their new streaming app. The purpose of this database is to provide Sparkify the ability to easily query data. 
    
    
# ER diagram & Data Modeling 
    In order to afford Sparkify's analytics requirements, The data engineering team understands that the best approach is star schema modeling. The star schema will allow a single fact table to keep track of user's interaction with the application. Also surrounded by some dimensions like songs, artists, users and time.
    
![Data Model](https://udacity-reviews-uploads.s3.us-west-2.amazonaws.com/_attachments/33760/1592532100/Song_ERD.png)


# ETL Process (pipeline) and Setup Project

***Important note:*** The files were ran on local machine with Postgres Server running on port = 8080

1. **etl.py**: Responsible for the orchestration of the entire data flow pipeline that will execute the extraction from JSON source files, transform data with DQ checks and load into Postgres tables; Note: When each time you run 'etl.py' it will execute automaticly the 'create_table.py' file, on function of drop_tables and create_tables.
2. **create_table.py** : Database and tables creation. It is necessary to be run before etl.py so the tables are created and cleaned;
3. **sql_queries.py** : Contains the creation table DDL and inserts DML scripts that will be called by create_table.py. It will drop any existing table before creating it again.
