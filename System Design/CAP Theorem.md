C - consistency 
A - Availablity
P - Partition Tolerance

P - Partition Tolerance
- Imagine having a datastore, for eg. they have 2 DBs, and both the DBs have the same data and users can access any of the database. In case of network partitions meaning there is a disconnect between the 2 DBs
Partition Tolerance - No replication for a particular node or group of nodes. Or it is called Isolated data i.e. data is isolated from other DBs in the distributed system.
![[Screenshot 2024-03-17 at 6.40.12 PM.png]]

Consistency
- Every user gets the same data, irrespective of which node they are querying from.
- Also called as same data.
- At a point in time, if multiple users query the same data it is called consistency.
![[Screenshot 2024-03-17 at 6.43.13 PM.png]]Availability:
- When a network partition happens in a distributed system, there is data inconsistency across the system, but the nodes are available. There is some data from teh distributed store.
- ![[Pasted image 20240317184950.png]]

![[Screenshot 2024-03-17 at 6.48.07 PM.png]]