# 5. Internal vs. External Data

## Overview

Eventsourcing requires a clear distinction between _internal_ and _external_ data. This distinction prevents coupling between systems.

__Example of bad practice__: Multiple apps directly read the database. As a result, any change in the database requires a rewrite of all applications. 

To prevent coupling systems too tightly, the solution is to define an API, creating an __Integration Event__

## Domain vs Integration Events

__Domain Events__ are living documents of the business behavior. These will evolve and change over time.

__Integration Events__ should be a stable summary of data. In order to implement changes over time, these events should be _versioned_.

By having an API, allows the creation of a contract on how the data is to be consumed. Again, _versioning_ will capture changes to the contract. Here, the version applies not to the system, but to the events.

### Changing the API

__Backwards Compatible__ change that allows consumers to still consume new event without adjustment. New optional attributes or mandatory attribute with default are backwards compatible. 

__Breaking__ change requires the consumer to update their behavior. Removing or renaming an attribute are breaking because the consumer needs to know about these in order to continue to read the data.

### Future proofing

Add a version to the streams.