# Explore Azure database and analytics services
## *Module 1 - 10 units*

- [Microsoft Docs for Module 1](https://docs.microsoft.com/en-us/learn/modules/azure-database-fundamentals/)
- [Microsoft Docs for LP2](https://docs.microsoft.com/en-us/learn/paths/az-900-describe-core-azure-services/)
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

### UNIT 3:  Explore Azure SQL DB
- Based on *latest stable version of MS SQL DB Engine*
- SQL - high performance, secure for *data driven appications n websites*
- ***FEATURES*** 
    - PaaS DB engine
    - DB management functions :  **upgrade, patch, backup, monitor**
    - 99.99 availability
    - Microsoft handles all updates to the SQL and operating system code. You don't have to manage the underlying infrastructure.
    - Concentrate on Domain Specific DB administration & optimisation for your business
    - Right choice for modern cloud apps, 
        - RDBMS and non relational like graphs, JSON, spatial, and XML    
    - Query processing - advanced features
        - in memory, high performance, intelligent query processing
        - newest SQL Server capabilities, with no overhead for updates or upgrades, tested across millions of databases
- ***Migration***
    - Tailwind currently has SQL servers on prem
    - These have data stored for public facing and internal only website
    - ***Azure Database Migration Service*** 
        - *Microsoft Data Migration Assistant can generate assessment reports* to guide the changes before migration
        - It performs all steps. You just change the connection string in your apps

--- 

### EXERCISE - UNIT 4 - CREATE a SQL DB on portal 
- Steps
    - *Create a resource > Databases > SQL database*
    - Tabs - Basic, Networking, Security, Additional settings, Review + Create
    - View deployment
    - Give firewall access to azure
- Learnt
    - Firewall rules
    - DB server and DB creation and test query

---

### UNIT 5: Explore Azure SQL Managed Instance
- ***Azure SQL Managed Instance***
    - Scalable cloud data service
    - Provides *SQL Server DB Engine compatibility with benefits of a PaaS*
- ***Features***
    - PaaS like Azure SQL DB (same features also)
    - Advantage of fully managed environment
    - Built-in high availability features and a 99.99% uptime service level agreement (SLA) + patching and version updates 
    - Automated backups and a configurable backup retention period
- ***Azure SQL Managed Instance provides several options that might not be available to Azure SQL Database*** 
- [Detailed comparison between SQL DB and Managed instance](https://docs.microsoft.com/en-us/azure/azure-sql/database/features-comparison)
- Eg: Cyrillic characters for collation in your on-prem
    - Azure SQL Database only uses the default SQL_Latin1_General_CP1_CI_AS server collation.
    - Difficult to move to a new DB on cloud
- ***Migration***
    - Migrate *on-premises data on SQL Server to the cloud using the **Azure Database Migration Service (DMS) or native backup and restore***
    - Same as on Azure SQL DB (just give connection string after assessing)
    - [Migration guide - SQL server to Managed instance](https://docs.microsoft.com/en-us/azure/azure-sql/migration-guides/managed-instance/sql-server-to-managed-instance-guide)


---

### UNIT 6: Explore Azure DB for MySQL
- ***Tailwind*** = used LAMP stack  (Linux, Apache, MySQL, PHP)
- *Already you know:*  Web Apps feature of Azure App Service provides built-in functionality to create web applications that use **PHP on a Linux server running Apache.**
- *Objective*: to find DB requirements are met or not
---
- ***Azure DB for MySQL***
    - *MySQL Community Edition database engine, versions 5.6, 5.7, and 8.0.*
    - 99.99 percent availability SLA from Azure
    - 24/7 running for app
    - built-in security, fault tolerance, and data protection
    - ***Additional***: point-in-time restore to recover a server to an earlier state, as far back as 35 days.
    - offers several service tiers, and each tier provides different performance and capabilities for diff workloads
    - Other normal cloud advantages....
---
### UNIT 7: Explore Azure Database for PostgreSQL
- ***Tailwind***
    - have been using PostgreSQL for several years
- *Objective:* Migrate to use Azure Database for PostgreSQL, and get same benefits as your on-premises server before moving to the cloud.
- ***Azure Database for PostgreSQL*** 
    - based on the community version of the open-source PostgreSQL database engine.
    - automatic backups and point-in-time-restore for up to 35 days
    - Enterprise-grade security and compliance to protect sensitive data at-rest and in-motion
        - covers SSL in network and data encryption on disk
    - Other normal advantages of SQL, MySQL etc. 
---
- ***Azure Database for PostgreSQL is available in two deployment options: Single Server and Hyperscale (Citus).*** 
- ***Single Server***
    - Vertical scale as needed, within seconds.
    - Other normal advantages
    - *Three pricing tiers: Basic, General Purpose, and Memory Optimized*
    - **Dynamic scalability** enables your database to transparently respond to rapidly changing resource requirements. (pay as you go)
- ***Hyperscale (Citus)***
    - The Hyperscale (Citus) option horizontally scales
    - queries across multiple machines by using *sharding*
        >Sharding is the process of **breaking up large tables into smaller chunks called shards** that are spread across multiple servers. A shard is essentially a **horizontal data partition** that contains a subset of the total data set, and hence is responsible for serving a portion of the overall workload.
    - great performance even when workload over 100GB data
    - Support for: *multi-tenant applications, real-time operational analytics, and high throughput transactional workloads*

---
### UNIT 8: Explore Big Data and Analytics
- *Tailwind needs*
    - GPS tracker for all delivery vehicles. Real time tracking data from sensors, weather n so on to primary data center
    - Aim: To get trends - ***look at several years data and find when there is a spike and need additional staff hires. Predict spikes during holidays etc.***
    - Your in-depth analysis is req for CTO to manage spikes
- *BIG DATA*
    - different forms and formats, large volume. 
    - Difficult to make sense of
- *Dealing with large data*
    - Open source cluster technologies are now developed.
    - MS Azure products
        ```
        Azure Synapse Analytics,
        Azure HDInsight,
        Azure Databricks,
        Azure Data Lake Analytics.
        ```
---
- ***[Azure Synapse Analytics](https://docs.microsoft.com/en-us/azure/sql-data-warehouse/)*** 
    - `formerly Azure SQL Data Warehouse`
- *Intro*
    - Enterprise Data warehousing + Big data analytics
    - Query in terms of 
        - *Serverless* or
        - *provisioned resources at scale*
    - Unified experience for immediate ***BI and ML needs***
---
- ***[Azure HDInsight](https://azure.microsoft.com/services/hdinsight/)***  
    - Open-source Analytics service for Enterprises
    - Easy, fast and cost effective to process massive data
    - Support popular Open source frameworks and cluster types like
        ```
        Apache Spark, Apache Hadoop, Apache Kafka, Apache HBase, Apache Storm, and Machine Learning Services.
        ```
    - Scenarios supported: 
        - Extraction, transformation, loading (ETL)
        - Warehousing 
        - ML
        - IoT
- ***[Azure Databricks](https://azure.microsoft.com/services/databricks/)*** 
    - Unlock insights from Data nad build AI solutions
    - Easy to 
        - ***set up Apache Spark env, autoscale and collaborate in interactive workspace***
    - Programming Lang: **Python, Scala, R, Java, SQL, libraries** such as *TensorFlow, PyTorch, and scikit-learn.*
- ***[Azure Data Lake Analytics](https://azure.microsoft.com/services/data-lake-analytics/)***  
    - On-demand analytics job service to simplify big data
    - Write queries to tranform and extract insights 
        - instead of *deploy, config and tune hardware*
    - Scale
        - *by setting dial for amt of power needed*
    - Pay as it is running = cost effective
---

### UNIT 9: Knowledge check
![image](https://user-images.githubusercontent.com/43994542/117778553-6323f100-b25b-11eb-81b3-03865b04b2b7.png)


---
### UNIT 10: Summary
- Azure services like
    - SQL DB, MYSQL, POSTGRES - FOR MIGRATING (WHILE PRESERVING DEV AND DB ADMIN STRENGTHS)
    - COSMOS DB - APIs FOR
        - MONGODB, CASSANDRA, TABLES, GREMLIN
    - BIG DATA AND ANALYTICS
        - SYNAPSE, DATALAKE, DATABRICKS, HDInsight
- Links to module for DB specific learning path
