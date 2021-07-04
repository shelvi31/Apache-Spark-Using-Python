# PySpark
Experiments with PySpark.

All that you need to understand before getting hands-on Apache Spark Data Processing Framework, read my medium blog: Link: https://garg-shelvi.medium.com/read-this-before-getting-started-with-apache-spark-5ffd61953a3d

![image](https://user-images.githubusercontent.com/66025137/124385353-be6ddf00-dcf2-11eb-878d-6f9609e7013e.png)
Whenever we learn a new tool/ technology, we all are in hurry to just skip the theory part to jump to implementation and coding. It is sometimes non-problematic and saves a lot of time but this cannot be the case if you are just starting with Apache Spark…
Before you actually start with the coding and implementation part of Spark it's very important to understand its components, usage, advantages, and other associated systems to actually know what and how to implement.
This Blog is all you need to start your journey with Apache Spark and Big Data Processing Framework.
Please Note: This Blog is mostly an adaptation of “Spark Tutorial by Simplilearn”, so if you want to read through the video instead, here’s the link.
In this blog you will read:
- Which are the Common Big Data data processing frameworks?
- What is Spark?
- Why Spark?
- Why is there a need for Spark?
- What are the limitations of Map Reduce in Hadoop?
- What are the components of a Spark Project?
- What is In-Memory Processing In Spark?
- What are the advantages and awesomeness of Spark over Hadoop?
- Terms you may encounter

Let’s get started….
Which are the common Big Data data processing frameworks?
1.Apache Hadoop MapReduce: Apache Hadoop (MapReduce) is a distributed and offline computing framework for parallel computing over big data, it is the core of the Hadoop data analysis framework.
2. Apache Spark: Spark is a distributed computing that depends on the MapReduce algorithm.
Spark is a well-known alternative for MapReduce and an extraordinary module to Hadoop. It is compatible with HDFS and Hive and can be integrated into the Hadoop ecosystem without any hazards or deficiencies of MapReduce.
Spark is written in the Scala language and uses Scala as its application framework. Spark and Scala are integrated together and Scala manipulate distributed data sets as easily as local collection objects. Spark improves usability by providing rich Scala, Java, Python API, R, and interactive Shell.
Spark provides services on batch mode, stream processing, interactive processing, graphics processing, and a one-stop platform for machine learning and other big data applications.
Other less known Data Processing frameworks:
3. Apache Flink
4. Apache Storm
5. Apache Tez
6. Apache Samza
etc…
![image](https://user-images.githubusercontent.com/66025137/124385340-b746d100-dcf2-11eb-8af4-ea62be658d0c.png)

Image Reference: Databricks
What is Spark?
Spark is a data processing framework.
History of Spark:
![image](https://user-images.githubusercontent.com/66025137/124385336-b31ab380-dcf2-11eb-8e1c-abcd08c2d6b8.png)

History of Spark: Image Reference
Note: Spark is both a real-time and batch processing Framework.
Why is there a need for Spark?
Main reason for Spark creation was to overcome the limitations with Map-Reduce.
![image](https://user-images.githubusercontent.com/66025137/124385331-aac27880-dcf2-11eb-99dc-b2fd06805f12.png)
![image](https://user-images.githubusercontent.com/66025137/124385334-ae55ff80-dcf2-11eb-9316-72ab087a6520.png)


Image Reference
Limitations of Map Reduce in Hadoop:
Map Reduce only does Batch processing.
Even Trial Operations Query is Complex, Key-value ( Reducer and mapper codes)
Unfit for large data on the network: Takes a lot of time in copying data which takes a lot of network bandwidth issues. Works on Data locality principle hence works well on the node where data resides.
Unsuitable for OLTP: as it works on batch processing mode it lacks latency for seconds and milliseconds.
Unfit for Graph Processing: Graphs represent structures to explore relationships between various points, for example: Finding friends in Social Media (Facebook Uses). Hadoop has Apache Giraph Library for such cases which run on top of Map-Reduce and add to the complexity.
As it is a state-less executor, it runs from the start every time, making it unfit for iteration processes.
Spark is an open-source cluster computing framework which addresses all of the limitations of map-reduce.
What are the Components of a Spark Project?
Spark Project mainly contains the following components:
Spark Core ( for batch processing)
Spark SQL (for interactive processing)
Spark Streaming (for stream processing)
Spark Graph x (for graph computing)
Spark MLlib (for machine learning)
![image](https://user-images.githubusercontent.com/66025137/124385316-a4cc9780-dcf2-11eb-9284-f137b0876a4a.png)

Image Reference
IN-DETAIL COMPONENTS OF A SPARK PROJECT:
Spark Core and RDDs: Are the foundation of the entire Spark Project, they provide basic I/O functionalities, distributed task dispatching, and scheduling.
RDDs are basic programing extractions and is a collection of data that is partitioned across machine logically. RDDs can be created by applying coarse-grained transformations on existing RDDs or by referencing external datasets.
Examples of these transformations are: reduce, join, filter and map.
The abstraction of RDDs is exposed similarly as in-process and local collections through language integrated APIs in Python, Java, or Scala. As a result of RDDs abstraction, the complexity of programming becomes simplified as the manner in which applications change RDDs is similar to changing local data collection.
2. Spark SQL: Spark SQL resides on the top of Spark Core. It introduces SchemaRDD, which is a new data abstraction and supports semi-structured and structured data.
SchemaRDD can be manipulated in any domain-based language(Python, Java, Scala) by Spark SQL. Spark SQL also supports SQL with Open Database Connectivity( ODBC) or Java Database Connectivity( JDBC) servers and command-line interfaces.
3. Spark Streaming: Spark Streaming leverages the fast scheduling capabilities of Spark Core for streaming analytics, ingesting data in small batches, and performing RDD transformations on them.
Because of this design, the same application code-set written for batch analytics can be used on a single-engine for streaming analytics.
4. MLlib: The 4th component of Spark is Machine learning Library, it lies on top of Spark and is a distributed ML framework. It can apply various common ML algorithms. With its memory-based architecture, it is 9x faster than Hadoop disk-based version.
5. GraphX: The last component GraphX also lies on the top of Spark, and is a distributed Graph Processing Framework. For computations of Graph, it gives an API and provides an Optimized Runtime for Pregel Abstraction. Pregel is a system for large-scale graph processing.
![image](https://user-images.githubusercontent.com/66025137/124385295-9ed6b680-dcf2-11eb-9e4b-ccc371ab19d9.png)

Image Reference
What is In-Memory Processing In Spark?
Spark provides 100x faster performance for applications with in-memory processing.
Let’s discuss applications for in-memory processing using column-centric databases. In column centric databases:
Similar data can be stored together: hence data can be stored with less memory and more efficiency.
Less memory usage: permits storing a large amount of data in the same space.
Increases the speed of processing: in in-memory database the entire database is loaded in the memory eliminating the need for indexes etc.
Avoids performance bottlenecks and slower database access: uses caching to speed up the query, caches are a subset of a very particular organized dataset.
As data lies completely in memory: analytics can be done by concurrent users within seconds.
Allows end-users and BA to create customized queries and reports
![image](https://user-images.githubusercontent.com/66025137/124385270-98483f00-dcf2-11eb-822e-088e16d12362.png)

Image Reference
All this leads to data access that is 10,000- 1,000,000 times faster as compared to disks!!!
![image](https://user-images.githubusercontent.com/66025137/124385264-91b9c780-dcf2-11eb-895f-1989b0e765ff.png)

Image Reference
What are the Spark Advantages:
Speed: Extend the map-reduce model to support stream processing and interactive queries.
Open-source cluster computing framework which addresses all of the limitations of map-reduce.
Suitable for real-time processing, trivial operation, processing large data on the network, OLTP, graphs, and iterative executions
100x fast than map-reduce
Fast Performance makes it suitable for ML as it allows programs to load and query data repeatedly.
Language Flexibility
![image](https://user-images.githubusercontent.com/66025137/124385235-89fa2300-dcf2-11eb-93b7-63aa3d224ede.png)


Image Reference
7. Combination: Spark covers various workloads that used to require different distributed system such as streaming, iteration, batch applications, as these applications are supported on the same engine, combining different processing types are easy. Spark is required in the production of data analysis pipelines, the combination feature allows easy management of separate tools.
8. Hadoop Support: Spark is capable of creating distributed datasets from any file that is stored in Hadoop Distributed File System( HDFS) or any other supported storage system.
Spark does not need Hadoop it just supports the storage system that implements the APIs of Hadoop.
Terms Encountered:
Scala is a strong statically typed general-purpose programming language that supports both object-oriented programming and functional programming.
Apache Hive is a data warehouse software project built on top of Apache Hadoop for providing data queries and analysis. Hive gives an SQL-like interface to query data stored in various databases and file systems that integrate with Hadoop.
HDFS: The Hadoop Distributed File System (HDFS) is a distributed file system. Apache Hadoop is a collection of open-source software utilities that facilitates using a network of many computers to solve problems involving massive amounts of data and computation. It provides a software framework for distributed storage and processing of big data using the MapReduce programming model.
![image](https://user-images.githubusercontent.com/66025137/124385214-7b137080-dcf2-11eb-9270-969e6ad3d422.png)

Image Reference: Data Flair
References:
Simplilearn, Spark Tutorial: https://www.youtube.com/watch?v=QaoJNXW6SQo
