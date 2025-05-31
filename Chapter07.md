# 7. Event Steaming, Event Sourcing and Stream Design

Event Streaming and Evert Sourcing are not the same.

__Event Streaming__ - this is data in _motion_. An example is Kafka. This is bringing data from point A to point B in a fast and reliable manner.

__Apache Kafka__ is a message broker with _producers_ and _consumers_, where messages are sent to a topic by the producer and the consumer subscribes to that topic to get these messages.

__Event Sourcing__ - is how to capture state changes in the system.
* __stream__ events that are grouped together by business logic.

## Designing Streams

To keep a stream manageable, there should be defined end to the stream.

