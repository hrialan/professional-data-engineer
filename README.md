# Google Certified Professional Data Engineer

## Storage and Databases

- Cloud storage
- Data transfer services
- Cloud SQL 
- Cloud Firestore
- Cloud Spanner
- Cloud Memorystore


## Big Data Ecosystem

- MapReduce
- Hadoop
- __Apache Pig :__
  - Platform for analysing large datasets
  - Language : Pig Latin
  - Abstaction for Map Reduce
  - Useful for creating ETL
  - Pig is a high level framework for running MapReduce jobs on __Hadoop__ clusters
- Apache Spark
- Apache Kafka


## Real Time Messaging with Pub/Sub

- Global messaging and event ingestion 
- Serveless
- 500 millions of messages per seconds
- "At least one delivery" guaranty
- Two types of subscription :
  - __Pull__ : default, messages must be acknowledged 
  - __Push__ : sent messages to an endpoint (HTTPS)
- Message retention default duration : 7 days (min : 10 min / max : 7 days)
- Messages must be 10Mb or less size


## Pipelines with Cloud Dataflow

- Powerfull ETL tool for transforming and enriching data
- Fully managed, serveless
- Uses open source Apache [Beam](https://beam.apache.org/) SDK
- Supports SQL, Java, Python
- Real-time and batch processing
- Stackdriver integration
- Data Source (Storage, BigQuery, PubSub, Kafka) -> Pipepline (Dataflow) -> Data Sink (Storage, BigQuery, Bigtable)

--- 
Cloud task 
