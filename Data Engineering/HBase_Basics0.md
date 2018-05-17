## HBase Basics

1. HBase is a NoSql datastore built on top of HDFS.
2. Provides us features like:
    * Reliability
    * Durability
    * Everything in HDFS and HBase is stored three times (Data Replication)
3. HBase is a column family oriented database.
4. Based on Google BigTable paper.
5. HBase Use Cases:
    * Need BigData TB/PB: Your application may scale to this size in future
    * High throughput: Millions of transactions/inputs per second
    * We want some columns to be variable
    * Allow random reads and writes
6. Not a good HBase use case:
    * If we want to read all the data in Petabyte size and analyze it all at once,
    generally not a good use case for HBase

## HBase Architecture:
