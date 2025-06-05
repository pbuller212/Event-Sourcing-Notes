# 3. Planning Systems Using Event Modeling

## Key Elements of Event Modeling

Taken from page 50. Red indicates that it is a pattern.

* __Events__ - Foundational building block of all information systems
* __Commands__ - Define the input parameters of the system. Commands are an instruction to the system to carryout a certain action.
* __Screens__ - These are the UX of the system. This is more about getting the required UI elements to represent the data, not about design and being pretty.
* __<span style="color: red;">State Change</span>>__ - combination of Events, Commands, and Screen (sometimes). Only way to trigger a change in the system.
* __Read Model__ - This is a query that gets data that is already stored in the system.
* __<span style="color: red;">State View</span>__
* __<span style="color: red;">Automation</span>__ - Actions in the system that are not triggered by an interaction.
* __External Event__ - Data that comes from an external system.
* __<span style="color: red;">Translation</span>__ - Ingesting data from an external source. Can be either a 
  * _Read Model_
  * _State Change_

__Information Completeness Check__ - Every attribute in a Read Model must have a source event.

__Given / When / Then__ (GWT) - Comes from behavior driven development to help define business rules. The form of these are "GIVEN something has already happened, WHEN this new thing happens, THEN we expect the system to be in this new state."