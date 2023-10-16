## Test for individual function in an object
- Simplest type of component
- Test == a set of call to the functions with different input parameters

## Test for object classes
- Design test case to cover all features in an object
- Testing in isolation of all operations associated with the object
- Setting and interrogation (tbh I think getting is a better word to use here) of all attributes
- Exercise of the object in all possible states

## Test for composite components
- Composite component -> made up of several different objects and functions
- Primary concern: Test the component interface behaves according to its specification
- Interface errors cannot be detected in individual object testing as errors may arise due to interactions between the parts
- Interface Testing
	- Parameter Interface Testing
		- Evaluation and validation of various parameters or inputs provided to a component
		- Ensure the component correctly processes and responses to different parameter values, within the valid ranges and at the valid boundaries of the ranges
	- Shared Memory Interface Testing
		- Shared Memory: Provide a way for different process of threads to read from and write to a common memory region
			- Allow for data exchange without the need of explicit message passing
		- Evaluate and verify the functionality, performance and reliability of communication interfaces which allow multiple processes or threads to access the shared memory region concurrently
	- Procedural Interface Testing
		- Procedural Interface: Component encapsulates a set of procedures to be called by another component
		- Examine and validate the communications which are happening between different procedural components or functions
		- Test to ensure different parts are able to collaborate correctly, produce the correct outcome as expected and adhere to defined specifications
	- Message Passing Interface Testing
		- Message Passing Interface: Data exchange or messages controlling which happens among different processes, threads or components in a distributed or concurrent software environment
		- Evaluate and verify communication mechanisms and interactions between different processes or components
		- Ensure messages are correctly sent, received and processed among different components