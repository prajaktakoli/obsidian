Horizontal Scaling - Buy more machines
Vertical Scaling - Bigger machines

Horizontal Scaling
- Load balancer required
- resilient
- Network calls hence slow
- Multiple systems can send requests to each other, so for eg. for any transaction DB needs to be locked. Hence data is inconsistent
- Scales well as users increases.

Vertical Scaling
- No load balancer required
- Single point of failure
- Interprocess communication
- Only 1 system on with data resides, hence data consistency is there
- Cannot extend the system after 1 point, hence hardware is limited

In real world, good qualities of both are used i.e. Hybrid model of scaling is used