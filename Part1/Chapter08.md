# 8. Domain Driven Design

__Domain Driven Design__ is a software development appraoch the emphasizes collaboration between business and technical teams, using a common language and clear definitions. Ideas can get lost in translation when different stakeholders play the telephone game. 

DDD aims to prevent this by creating a __Ubiquitous Language__. This language has a __Bounded Context__ whore outside of this boundary, the ubiquitous language is not spoke.

Event Modeling does this by understanding how data flows through the system.

In the DDD world, an __aggregate__ is a cluster of domain objects that can be treated as a single unit. 
* Root Entity - main point in accessing other entities within the aggregate
* Boundary - entities within this boundary are allowed to interact with each other
* Consistency Rules - this is enforced only within the boundary of the aggregate
* Transaction Scope - changes must be atomic, completed with a single transaction
* References - entities outside the aggregate should only interact with root entity




