# DDIA page 361

## Distributed Transactions in Practice

2PC perfomance issuse caused by additional disk forcing that is required for crash recovery.&#x20;

### database internal distributed transactions

internal transactions among the nodes of the database

### Heterogeneous distrubted transactions

Participatians are two or more different technologies, like message queue and database



## Exactly-once message processing

A message from a message queue can be acked iff the database transaction for processing the message was committed successfully. Perfomed by atomically committing and database writes in a single trancation



### Holding locks while in doubt

A transaction must hold onto the locks throughout the time it is in doubt. Sometimes forever



## Fault-Tolerant Consensus

The key is Termination, every node that does not crash eventyally decides some value.



Many algorithms are using total order broadcast to achive fault tolerant consensus.





