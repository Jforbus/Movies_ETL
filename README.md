# Movies_ETL

## Project Overview
Performing Extract Transform and Load functions on Movie data collected from Wikipedia and Kaggle to create a database for research and analysis of the Movie data.  

### Resources
- Data Source: wikipedia-movies.csv, movies_metadata.csv, ratings.csv
- Software: Python 3.7.1, Anaconda 4.14.0, Jupyter Notebook 6.4.8, Pandas 1.4.3, PostgreSQL 14, pgAdmin 4

## Results
Data from 3 CSV files containing a large amount of historical data on Movies, TV shows, and other media products is cleaned, merged, and imported into a PostgreSQL database.
Two tables are created within the database. The first, titled `movies`, includes a dataset covering 31 data points for 6052 movies, trimmed to exclude missing, erroneous or irrelevant data.
![movies_query](https://github.com/Jforbus/Movies_ETL/blob/main/Resources/movies_query.png)

An additional table is created within the pipeline that is not included within the database. This DataFrame merges the above `movies` table with the ratings data with for the movies included. This DataFrame breaks down the ratings into groups and provides a count of the total ratings within each group a movie received.


The second table, titled `ratings`, is a complete dump of the ratings.csv file. The ratings data is included in a merged DataFrame for the movies listed, however the file contains over 26,000,000 ratings for media products. Given the purpose of the database, the ratings table was created including the complete ratings dataset for additional research availability.
![ratings_query](https://github.com/Jforbus/Movies_ETL/blob/main/Resources/ratings_query.png)

