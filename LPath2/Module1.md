# Explore Azure database and analytics services
## *Module 1 - 10 units*
---
### UNIT 1: Introduction
- ***Tailwind needs***
    - CTO officer wants you to research database options
    - Application need: 
        - ***responsive, always online, low latency, availablity***
        - deploy in datacenters close to users  
        - respond to usage at peak hours and increasing data volume and give users data in milliseconds. 
        - Azure is perfect 
            - *global distribution, support for industry std DBs and APIs*
- ***Video contents***
    - Relational, NoSQL, inmemory
    - Infra management 
    - New DB or migrate existing DB (SQL, mySQL)
    - Cosmos DB - migrate cassandra n mongo DB
    - Cache for Redis 
    - Guide for migration service
- ***Learning objectives***  
    - Azure Cosmos DB
    - Azure SQL Database
    - Azure SQL Managed Instance
    - Azure Database for MySQL
    - Azure Database for PostgreSQL
    - Azure Synapse Analytics
    - Azure HDInsight
    - Azure Databricks
    - Azure Data Lake Analytics



---
### UNIT 2: Explore Azure Cosmos DB
- Teams of developers who used different database services and various APIs to work with their data
    - common database service - Azure Cosmos DB
- ***Azure Cosmos DB*** 
    - Global distributed, Multi model DB service
    - Elastically and independently scale across regions
    - SLAs for throughput, latency, availability and consistency
    - API for single digit millisecond access
---
    - Schema less, "Always on " application support for constantly changing data
    - Eg: Tailwind has Public training portal used by customers - 
        - frequently updating online catalog 
    - At the lowest level, Azure Cosmos DB stores data in atom-record-sequence (ARS) format
    - The data is then abstracted and projected as an API (flexible for developer choice)
    - Choice for DB: *SQL, MongoDB, Cassandra, Tables, and Gremlin*
---
