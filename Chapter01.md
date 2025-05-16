# 1. Why you should care

## Definitions

* __Events__ are immutable, onve they happen they cannot be changed.
* __Event Stream__ is the chronological sequence of all state changing events.
* __Projection__ is a way to create a view of an event stream.
* __Event Store__ is the component that stores event streams. Supports only __Append__ and __Read__ operations.

# 2. Event Sourcing - What is it?

There are no schemas or data modeling up front. It is not possible to get this right the first time around.