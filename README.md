hive-json
=========

Contains twitter data, tool to load into HDFS, hive schema, and sample queries for extracting tweets

Prerequisites
-------------
1. HDFS and YARN
2. Hive
3. org.apache.hcatalog.data.JsonSerDe on the classpath (hcatalog*core.jar)
4. Tez (optional)

To run:
------------------
Load the sample data into HDFS

`./load_data_into_hdfs`

Create the hive table

`hive -f create_table.hsql`

Run the test query with Hive MR

`hive -f tweets_query.hsql`

Run the test query with Hive Tez (optional)

`hive -f tweets_query.hsql -hiveconf hive.execution.engine=tez`

