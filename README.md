1. Discuss the purpose of this database in the context of the startup, Sparkify, and their analytical goals.
2. State and justify your database schema design and ETL pipeline.
3. [Optional] Provide example queries and results for song play analysis.

## 1. the purpose of this database

the purpose of this database is for understanding what songs users are listening to.

## 2. reason for schema design and ETL pipeline

- Fact table: songplays
    - this is the purpose of design
- Dimension Tables
    - users
    - songs
    - artists
    - time

### simple diagram

```
log data ----[extract and transform]--------> load time table
                                       -----> load users table
                                       -----> load songplays table
                              
song data ----[extract and transform]-------> load songs table
                                       -----> load artists table
```

### how to run ETL pipeline

```
> python3 create_tables.py 
> python3 sql_queries.py 
> python3 etl.py 
```