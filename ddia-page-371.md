# DDIA page 371

## Membership and Coordination Services

They provide Key-Value API like get, put, delete, range-over-keys

### Zookeeper

* Linearizable atomic operations.
* Total ordering of operations.
* Failure detection.
* Change notification.

### Allocating work to nodes

* Zookeeper can be used to select which node to be the next leader
* Zookeeper needs to decide which partition to assign to which node and also want fault tolerant.

### Service discovery&#x20;

To find out which IP address you need to connect to in order to reach a particular service.

###

