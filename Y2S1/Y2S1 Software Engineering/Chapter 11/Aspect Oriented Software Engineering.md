Topic: [[Y2S1 Software Engineering]]

## Separation of Concerns
- Concern -> a logical requirement or a set of requirements
- Organise software so that each element in the program does one and only one thing
- Stakeholder concerns
	- Functionality
		- In a train control system -> train braking
	- Quality of Service
		- Performance
	- Policy
		- Security, safety, business rules
	- System
		- Maintainability
	- Organisational
		- Software within budget, maintain reputation

## Cross-cutting concerns
- Core concerns
	- Functional concerns that relate to the primary purpose
- Secondary Functional Concerns
	- Non-functional requirements

## Problem with Programming Language Abstraction
- Tangling
	- When a module in a system includes code that implements other system requirements
- Scattering
	- When the implementation of a single concern is scattered across several components in a program
	- Likely to occur when requirement related to secondary functional concerns or policy concerns are implemented
- Why tangling and scattering is a problem
	- When System Requirement Specification change, need to spend more time looking for the components to change, and is expensive

## Aspects, Join Points, Point cuts
- Advice (code)
	- Action taken by an aspect
	- Type of advice: before, around, after
- Aspect 
	- Modularisation of a concern that cuts across multiple classes
	- Allow to separate the cross-cutting concerns from the main business logic of a program
	- Makes code more modular, maintainable and easier to understand
	- Define concern, point cuts and advice associated with concern
- Join Point (Event)
	- A point during execution of a program
	- Eg.
		- Execution of a method
		- Handling of an exception
- Point cut
	- A set of join points
	- Define specific points in the execution flow of a program, where an aspect should be applied
	- Use expressions to specify which join points are of interest
	- Advice is associated with a point cut and runs at any join point matched by a point cut
	- Eg.
		- Execution of a method with a certain name
- Weaving
	- Process of integrating or applying aspects to the appropriate join points in a program's execution flow
	- Incorporation of advice code at the specified join points by an aspect weaver
- Join Points Model
	- A set of events
	- Eg
		- Call Event
		- Execution Event
		- Initialisation event
		- Data event
		- Exception event
- Aspect woven
	- Responsible to include advice at the join points specified in the point cuts

## Software Engineering with Aspects
- Core system design
	- Design system architecture to support core functionality of the system
	- Take into account quality of service requirements like performance and dependability
- Aspect identification and design
	- Start with the extensions identified in system requirements
	- Analyse to see if they are aspects as their own or needs to be broken down into several aspects
- Composition design
	- Analyse core system aspect designs to discover where the aspects should be composed with the core system
	- Identify join points in a program at which aspects will be woven
- Conflict analysis and resolution
	- Aspects may interfere with each other when they are composed with the core system
	- Conflicts occur when there is a point cut clash with different aspects specifying they should be composed at the same point into the program
	- When aspects are designed independently, they may make assumptions on the core system functionality that has to be modified
	- When aspects are composed, one may affect the functionality of a system not anticipated by other aspects
	- Overall system behaviour may not be as expected
- Name design
	- Define standards for naming entities in the program
	- Essential to avoid accidental point cuts
		- Occurs when at some program join point, name accidentally matches that in a point cut pattern

## Verification vs Validation
- Verification
	- Process of determining whether products of a given phase of the software development process fulfil the requirements established during previous phase
	- Normally is defect prevention
	- Are we building the system right
- Validation
	- The process of evaluating software at the end of software development to ensure it complies with the intended usage
	- Normally is defect detection
	- Are we building the right system