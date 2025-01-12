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
While the DB is executing the query, the thread will serve anotehr request.
When the DB prepares the message, it will put a message on the Event Queue, node is continously monitoring the queue in the background, if it finds it in the queue, it will take it out and process it
used for i/o intensive applications
not ideal for CPU intensive applications like video editing etc