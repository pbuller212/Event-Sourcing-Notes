# 10. Vertical Slicing

A __vertical sliced architecture__ is something where coupling between slices is minimized, but within the slice the coupling is maximized.

__Open-Closed Principle__ and part of the system should be open for _extension_, but closed for _modification_.

If parts of the system are __coupled__, then a change in one part requires a change in another.

The classic method to architect a system is to divide it into layers
1. Presentation
1. Service
1. Persistence

Vertical slicing is more like a microservice architecture, and the three layers are packaged into a slice that represents a singular piece of functionality. 

Vertical Slicing and Event Modeling are separate concepts, but they work well together.

Benefits of Vertical Slicing:
1. clearly structured codebase
1. minimizes coupling
1. scalable development
1. testable codebase

Drawbacks can be
1. Duplicated code
1. lack of tooling




