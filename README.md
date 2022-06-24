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
- Pipelines are DAGS
- A PCollection is a data set or data stream. The data that a pipeline processes is part of a PCollection
- Window - A PCollection can be subdivided into windows based on the timestamps of the individual elements. Windows enable grouping operations over collections that grow over time by dividing the collection into windows of finite collections.
- Watermark - A watermark is a guess as to when all data in a certain window is expected to have arrived. This is needed because data isn’t always guaranteed to arrive in a pipeline in time order, or to always arrive at predictable intervals.
- Trigger - A trigger determines when to aggregate the results of each window. For bounded data, results are emitted after all of the input has been processed. For unbounded data, results are emitted when the watermark passes the end of the window, indicating that the system believes all input data for that window has been processed.
- [Documentation](https://beam.apache.org/documentation/basics/)

## Managed Spark with Cloud Dataproc

- Dataproc is a fully managed and highly scalable service for running Apache Spark, Apache Flink, Presto, and 30+ open source tools and frameworks.
- Use Dataproc for data lake modernization, ETL, and secure data science, at planet scale, fully integrated with Google Cloud, at a fraction of the cost.

- Dataproc is a great choice for quickly migrating Hadoop and Spark workloads into GCP.
- Biggest benefits of Dataproc -> ease of scaling, being able to use Storage instead of HDFS, and the connectors to other GCP services including BigQuery and BigTable.
- Hadoop, Spark, Zookeper, Hive, Tez, Jupyter
- Often Dataflow is a prefered product for ingesting Big Data, in particular for streaming. 

## NoSQL Data with Cloud Bigtable

- Managed wide-columns NoSQL Database (key value pairs)
- High throughput
- Low latency
- Scalability
- High availability

- HBase -> open source implementation of the big table model / now a top-level Apache project

- Every row has a key which identifies it. The only index you get. 
- Each row can have several columns which can be grouped into families.
- Empty cells don't use any space in the database.

- Particularly well suited for marketing, financial and transactional data. (purchase histories, stock prices) 
- Also for Time Series and IoT.
- For at least a terabyte of storage
