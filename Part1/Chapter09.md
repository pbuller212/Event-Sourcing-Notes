# 9. Handling Transactions in distributed systems using Sagas

__Sagas__ are used to coordinate across systems. One place they show up is in Microservice Architectures.

The problem statement is that if systems are decoupled, then there is no concept of a transaction like there would be in a single database. __Sagas__ are an attempt to fix this problem.

## Solution 1 - Process Coordinator

Process Coordinators are orchestrators that has a central instance and manages the flow. The issue is that this creates coupling between the coordinator and this different systems.

## Solution 2 - Service Autonomy

Service Autonomy means choreagraphy. The idea is that a system sends notice that an event has happened. Handling this notice is on the other systems. One issue with this setup is that it can be hard to debug.




