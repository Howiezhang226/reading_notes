# DDIA page 421

## Beyond MapReduce

It is hard to implement some mapreduce algorithms, like join.

There some alternatives. Many abstractions were created, such as Pig, Hive, Cascading, Crunch to make this task easier.



### Materialization of Intermediate State

It is bad to persist intermediate state all the time.

### Dataflow Engine

spark, flink&#x20;

data flow engine: explicitly model the flow of data through several processing stages.

### Fault Tolerance

Spark, Flink and Tez avoid writing intermediate state to HDFS,  they need other approaches to do FT.

### Nondeterminism

Nondeterministic operation, such as iterating a hash table, can result a different copy of the data.



