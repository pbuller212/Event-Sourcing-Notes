# 4. CQRS, Concurreny, Consistency

## Basic tenants

* __CQRS__ - command/query responsibility segregation
* __CQS__ - every method in a system should be either a command or a query, ___but never both___

## Basic definitions

A __Command__ is an oepration that alters the state of the system.
 * processing an order
 * add an item to the shopping cart

A __Query__ retreives data from the system, but does not alter the state.

## What is CQRS

__CQRS__ is a pattern for software architecture that implements CQS at the system level.

Read and write operation are left separate. While not requiring separate data stores, this allows for a read store and a write store.

## Consistency challenges

The problem with keeping separate data stores is that keeping the two _consistent_ becomes a challenge. A single source of truth must be created, the __Event Store__.

__Concurrency__ is when two attempts are made to write to the same piece of data. The answer to this problem is to use _locking_.

__Optimistic locking__ is checking nothing has changed to my version of the data, but does not implement an actual lock.

An example of optimistic locking is source control using git. When a file is "checked out", others can edit the file. It is when the file is "checked in" that differences are detected.

Event sourcing uses optimistic locking on individual event streams.
