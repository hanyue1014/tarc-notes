Topic: [[Y2S1 Software Engineering]]

## What is Real Time System
- A software system that functions depends on **result produced** and **time that the results are produced**
- E.g.
	- Air traffic control system
	- Autonomous driving systems
- [[Soft Real Time System]]
- [[Hard Real Time System]]

## Stimuli of Real Time System
- Have to respond to events (stimuli) at irregular intervals
- These stimuli often causes the system to move to another state
- Can be used as a way of describing a state machine modelling real time system
- State model
	- Assumes that at any time the system is in one of the possible states
- One way of looking at real time system -> [[Stimulus Response System]]

## Stages of Real Time System Design
- Identify the stimuli that the system must process and the associated responses
	- Stimuli: Intruder Alarm
	- Response
		- Call to police
		- Switch on light
		- Notify owner
	- Priority level of stimuli
		- Highest: Interrupt level -> allocated to processes that require a very fast response
		- Clock level -> Allocated to periodic processes
- Identify timing constraints for each identified stimuli and response
- Combine the stimulus and response processing into a number of concurrent processes
- Design an algorithm for each stimulus and response
- Design a scheduling system to ensure that processes are started in time and meet their deadlines
- Integrate the system under the control of a [[Real Time Operating System]]

## Control Models
- Time triggered control
	- Executes the control actions at the scheduled time intervals
	- Ensures the deterministic and predictable system behaviour
	- Applicable to safety critical system -> chemical plant real time monitoring system
- Event driven control
	- Triggers system's control action based on specific events or conditions
- Adaptive control
	- Adjusts the control parameters based on system's behaviour
	- Enable adaptation towards any changes in the system
	- More suitable for uncertain behaviour system
- Fuzzy logic control
	- Uses fuzzy rules to handle imprecise and uncertain inputs from the end users
	- Suitable for the system's behaviour that is difficult to be modelled precisely

## Additional (dk shud categorise under where)
- [[Monitoring and Control Systems]]