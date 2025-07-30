# SQL London Transport Analysis

Analysis of London public transport journey data using SQL.

## Project Description

London’s multi‑modal transport network (buses, Underground, DLR, Overground, trams, river services, etc.) is operated by Transport for London (TfL). In this project you will:

1. Load and analyze the `TFL.JOURNEYS` dataset (provided as CSV).  
2. Answer three key questions:  
   1. Which transport modes are the most popular overall?  
   2. When was Emirates Airline (the cable car) most used?  
   3. Which years saw the lowest usage of Underground & DLR?  
3. Write clean SQL queries for aggregation, filtering, and ordering.

## Repository Structure

├── assets/ – images used in README or documentation
│ ├── london.jpg
│ └── tube.jpg
├── data/ – source CSV exported from DataCamp
│ └── tfl_journeys_final.csv
├── notebooks/ – exported Jupyter notebooks from DataCamp
│ └── Exploring_London_Travel_Network.ipynb
├── sql/ – production‑ready SQL scripts
│ ├── 01_most_popular.sql
│ ├── 02_emirates_trends.sql
│ └── 03_least_popular_tube.sql
└── README.md – project overview and instructions
## How to Run

1. Load the CSV file into your SQL environment (e.g., into a Snowflake table `TFL.JOURNEYS` or into any local SQL database).  
2. Execute the SQL scripts in the `sql/` folder in order:
   ```sql
   -- In your SQL client:
   COPY INTO TFL.JOURNEYS
     FROM 'data/tfl_journeys_final.csv'
     FILE_FORMAT = (TYPE = CSV FIELD_OPTIONALLY_ENCLOSED_BY = '"' SKIP_HEADER = 1);

   -- Then:
   @sql/01_most_popular.sql
   @sql/02_emirates_trends.sql
   @sql/03_least_popular_tube.sql
3. View results in table form or export to CSV as needed.
## Technologies & Tools

   - SQL (Snowflake dialect or standard SQL)

   - Data Source: CSV (data/tfl_journeys_final.csv)

   - Platform: DataCamp Workspace (analysis), Snowflake or local SQL engine (production)

   - Documentation: Markdown, Jupyter Notebooks


## Key Outputs

   - most_popular_transport_types: total journeys per transport mode

   - emirates_airline_popularity: top 5 month–year records for Emirates Airline

   - least_popular_years_tube: five years with lowest Underground & DLR usage
