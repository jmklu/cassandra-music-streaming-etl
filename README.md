# Data Modeling with Cassandra for Sparkify's Music Streaming App

## Project Overview

This project builds a NoSQL database using Apache Cassandra to model and query large-scale event data for Sparkify, a music streaming app. The goal is to efficiently store user activity data and enable optimized querying for analytics teams. This project is part of the Udacity's Data Engineering Nanodegree.

## Key Features

- **NoSQL Data Modeling**: Designed and implemented denormalized data models in Apache Cassandra to handle large volumes of event data.
- **ETL Pipeline**: Developed an Extract, Transform, Load (ETL) pipeline using Python to preprocess event data from CSV files and load it into Cassandra tables.
- **Optimized Queries**: Designed tables with partition keys and clustering keys using Cassandra Query Language (CQL) to optimize query performance and support analytics use cases.

## Project Structure

- **event_data**: Contains the raw CSV files with user activity data.
- **etl_pipeline.ipynb**: Jupyter Notebook implementing the ETL pipeline to preprocess and load data into Cassandra tables.
- **queries.txt**: Contains example queries run against the Cassandra database to extract insights from the data.

## Data Modeling

Three main tables were created in Cassandra to address the specific analytical queries:
1. **songplays_by_session**: Retrieves the songs played in a session.
2. **user_song_history**: Tracks the history of songs a user has listened to.
3. **songplays_by_user**: Allows analytics to track songs played by each user, ordered by session and timestamp.

## ETL Pipeline

The ETL pipeline performs the following steps:
1. Reads multiple CSV files containing event data from `event_data` directory.
2. Preprocesses and cleans the data, creating a consolidated file.
3. Inserts the cleaned data into the relevant Cassandra tables.

## Getting Started

### Prerequisites

- Apache Cassandra installed and running locally or on a remote cluster.
- Python 3.x and the following libraries:
  - `pandas`
  - `cassandra-driver`

