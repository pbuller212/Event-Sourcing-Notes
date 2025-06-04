# 7. Event Steaming, Event Sourcing and Stream Design

Event Streaming and Evert Sourcing are not the same.

__Event Streaming__ - this is data in _motion_. An example is Kafka. This is bringing data from point A to point B in a fast and reliable manner.

__Apache Kafka__ is a message broker with _producers_ and _consumers_, where messages are sent to a topic by the producer and the consumer subscribes to that topic to get these messages.

__Event Sourcing__ - is how to capture state changes in the system.
* __stream__ events that are grouped together by business logic.

## Designing Streams

To keep a stream manageable, there should be defined end to the stream. This helps prevent large chunks of data from forming, and mirrors the accouting idea of "Closing the books." This forms a boundary where validation can occur

The ability to modify the stream design is one of the strengths of event sourcing, as provides flexibility when things need to change.

__Every string has a unique identifier__

When laying out streams, using swinlane diagrams is useful.The lane defines the boundary of the stream. 

To validate the stream design, read the events from left to right in the swimlane, and they should ring true to someone's common sense of the process. 

Another trick is to verify that each event has all the information it needs from the previous events. If this cannot be done, the information source must be identified. 

