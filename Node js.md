-A runtime environment for executing javascript code

Node architecture:
![[Pasted image 20250112174530.png]]----------------------------------------------------
How Node works:
-------------------------------------------

- Node is not a programming language and also not a framework.
Features:
1. It is not blocking
2. Asynchronous
A single thread will handle the multiple request
![[Pasted image 20250112213724.png]]

A single thread will serve the Request. If the request has to query the DB, the thread will not wait for the request the data