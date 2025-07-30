# SQL London Transport Analysis

Analysis of London public transport journey data using SQL.

## Project Description

London’s multi-modal transport network (buses, Underground, DLR, Overground, trams, river services, etc.) is operated by Transport for London (TfL). In this project you will:

1. Load and analyze the `TFL.JOURNEYS` table from a Snowflake database, which contains:
   - **MONTH** — month number (1 = January)  
   - **YEAR** — year  
   - **DAYS** — number of days in the month  
   - **REPORT_DATE** — reporting date  
   - **JOURNEY_TYPE** — transport mode  
   - **JOURNEYS_MILLIONS** — journeys in millions  

2. Answer three key business questions:
   1. Which transport modes are the most popular overall?  
   2. In which months/years was Emirates Airline (the cable car) most used?  
   3. Which years saw the lowest usage of Underground & DLR?  

3. Write clean SQL queries for aggregation, filtering, and ordering of results.

## Repository Structure

/
├── README.md – this file
├── sql/ – SQL scripts
│ ├── 01_most_popular.sql
│ ├── 02_emirates_trends.sql
│ └── 03_least_popular_tube.sql
└── data/ – Snowflake connection instructions
└── connection_guide.md


## Technologies & Tools

- **SQL** (Snowflake dialect)  
- **Database**: Snowflake  
- **Platform**: DataCamp Workspace (exported locally)  
- **Documentation**: Markdown  

## How to Run

1. Follow the steps in `data/connection_guide.md` to configure your Snowflake connection.  
2. Execute the SQL scripts in the `sql/` folder in order (01 → 02 → 03).  
3. View query outputs as tables or export them as CSV.

## Key Outputs

- **most_popular_transport_types**: total journeys by transport mode  
- **emirates_airline_popularity**: top 5 month–year combinations for Emirates Airline  
- **least_popular_years_tube**: five years with lowest Underground & DLR usage  

