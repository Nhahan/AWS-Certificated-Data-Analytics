# AWS Certificated Data Analytics

- Real Time
  - Kinesis Data Streams (KDS)
  - Simple Queue Service (SQS)
  - Internet of Things (IoT)

- Near-real time
  - Kinesis Data Firehose (KDF)
  - Database Migration Service (DMS)


Kinesis
  -
Kinesis is a managed alternative to <b>Apacha Kafka</b>
  - Kinesis Streams: low latency steraming ingest at scale
  - Kinesis AnalyticsL: optionally perform real-time analytics on streams using SQL
  - Kinesis Firehose: load(store) streams in S3, Redshift, ElasticSearch & Splunk(near real-time)
![image](https://user-images.githubusercontent.com/81916648/146720480-9107a03e-6ffb-4837-b559-8558a9f98713.png)

Kinesis Operations 
  -
- Adding Shards (Also called "Shard Splitting"
  - Can be used to increase the Stream capacity (1 MB/s data in per shard)
  - Can be used to divide a "hot shard"
  - The old shard is closed and will be deleted once the data is expired

- Merging Shards
  - Decrease the Stream capacity and save costs
  - Can be used to group two shards with low traffic
  - Old shards are closed and deleted based on data expiration

- Limitations
  - This not operated automatically
  - It takes time to scale up or down (ex. 1000 shards to 2000 takes 8.3 hours)


Redshift
  -
