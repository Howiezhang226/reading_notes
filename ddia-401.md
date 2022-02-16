# DDIA 401

## MapReduce and Distributed Filesystems

MapReduce sort of like Unix tools, but runs on a distributed system. It takes immutable input files and produce immutable output files and do no have other side effects.



### MapReduce Job Execution

Mapper The mapper function is called once for every input record, and the function will extract the key, value pair from the record and generates a number of key-value pairs.



Reducer The reduce takes a list of key-value pairs where all the value that belong to the same key is combined in one list. Reducer function produces a collection of values from each key-values pair.



MapReduce will automatically sort the key produced by Mapper



### Distributed execution of MapReduce



Reduce-Side Joins and Grouping

It will be very slow if we do a naive join between two database because the network through. A better solution is would be to take a copy of the user database  and to put it in the same distributed filesystem as the log of user activity events. You would then have the user database in one set of files in HDFS and the user activity records in another set of files, and you could use MapReduce to bring together all of the relevant records in the same place and process them efficiently.



Sort-merge joins

Reduce side join. Reducer will have a secondary sorted (dob first, url next) key-values pair. It has all the information for one user, and never need to make requests over the network.



Handling skew&#x20;

How to solve hot key problem?

Skewed join&#x20;

When performing the actual join, the mappers send any records relating to a hot key to one of several reducers, chosen at random. For the other input to the join, records relating to the hot key need to be replicated to all reducers handling that key
