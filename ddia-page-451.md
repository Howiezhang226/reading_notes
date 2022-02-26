# DDIA page 451

## Databases and Streams



We can apply the idea of streams to database. The event of writing something to a database is an event.



### Keep Systems in Sync

We have multiple systems too satisfy storage, querying, processing requirements.

How can we keep these systems in sync.

Dual write is not an idea because of write conflicate.&#x20;

### Change Data Capture

The process of observing all data changes written to a database and extracting them in a form in which they can be replicated to other systems.



### Initial snapshot

Snapshot is important to build a new full-text index because we don't want to store all the logs&#x20;

### Log compaction

A background process consistently scan the log and throw away duplicates and keep only the most recent update for each key.

