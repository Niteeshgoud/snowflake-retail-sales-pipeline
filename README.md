\# Snowflake Retail Sales Data Pipeline



A hands-on data engineering project demonstrating an end-to-end

data pipeline using Snowflake, SQL, and Power BI.



\## Architecture



CSV Files

→ Snowflake Internal Stage

→ RAW Layer

→ STAGING Layer

→ ANALYTICS Layer

→ Power BI



\## Source Data



The project uses four CSV files:



\- customers.csv

\- products.csv

\- orders.csv

\- order\_items.csv



\## Data Pipeline



\### 1. Data Ingestion



CSV source files are uploaded into a Snowflake internal stage.



The data is then loaded into RAW tables.



\### 2. RAW Layer



The RAW schema stores source data:



\- RAW.CUSTOMERS

\- RAW.PRODUCTS

\- RAW.ORDERS

\- RAW.ORDER\_ITEMS



\### 3. STAGING Layer



The staging layer performs basic data cleaning and standardization,

including:



\- Trimming text values

\- Standardizing order status

\- Preparing source data for downstream transformations



Tables:



\- STAGING.STG\_CUSTOMERS

\- STAGING.STG\_PRODUCTS

\- STAGING.STG\_ORDERS

\- STAGING.STG\_ORDER\_ITEMS



\### 4. ANALYTICS Layer



The analytics layer combines customer, order, order item,

and product data into a reporting-ready sales dataset.



Business logic includes:



\- Joining customer, order, product, and order-item data

\- Excluding cancelled orders

\- Calculating total sales amount



Revenue calculation:



TOTAL\_AMOUNT = PRICE \* QUANTITY



Final table:



ANALYTICS.SALES\_REPORT



\### 5. Reporting



Power BI connects to the Snowflake analytics layer.



The report contains:



\- Revenue by Product

\- Revenue by Category



\## Technologies Used



\- Snowflake

\- SQL

\- Power BI Desktop

\- Git

\- GitHub



\## Project Purpose



This project was created as part of my hands-on Snowflake and

Data Engineering learning journey.



The goal was to understand how source data moves through ingestion,

raw, staging, analytics, and reporting layers rather than practicing

Snowflake SQL commands in isolation.

