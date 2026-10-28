# Yelp Data Engineering Pipeline: Python, AWS S3 & Snowflake

## Project Overview

This project demonstrates a data engineering workflow using Python, Amazon S3, and Snowflake to process Yelp JSON data and perform SQL-based analysis.

The pipeline includes splitting large JSON files into smaller files, storing the processed data in Amazon S3, loading JSON data into Snowflake, transforming semi-structured data into structured tables, and analyzing review sentiment.

## Architecture

1. **Python** — Splits large Yelp JSON data into smaller files.
2. **Amazon S3** — Stores the processed JSON files.
3. **Snowflake** — Loads the JSON data using an external stage and storage integration.
4. **SQL transformations** — Extracts business IDs, review dates, user IDs, star ratings, business details, and other fields.
5. **Sentiment analysis** — Uses a Snowflake SQL function to analyze review sentiment.
6. **SQL analysis** — Answers business-related questions using the transformed data.

## Technologies Used

- Python
- Jupyter Notebook
- Amazon S3
- Snowflake SQL
- Semi-structured JSON data
- Git and GitHub

## Repository Contents

- `Yelp Files Split.ipynb` — Notebook for splitting Yelp JSON data.
- `Table-yelp_reviews.sql` — Review data loading and transformation.
- `Table-yelp_businesses.sql` — Business data loading and transformation.
- `Function-analyze_sentiment.sql` — Sentiment analysis function.
- `Questions.sql` — SQL analytical queries.
- `.gitignore` — Excludes environment files and generated files from Git.

## Security

AWS credentials are not included in the SQL scripts. The Snowflake stage is intended to use a storage integration rather than hardcoded AWS access keys.

Configure your own AWS resources and Snowflake storage integration before running the loading scripts.

## Notes

The Yelp source dataset is not included in this repository. Users must obtain the data separately and configure their own S3 bucket and Snowflake environment.

This repository documents the project implementation; end-to-end execution should be verified in the user's own environment.
