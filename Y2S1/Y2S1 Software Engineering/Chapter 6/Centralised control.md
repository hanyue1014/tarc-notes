- One sub-system has overall responsibility for control and starts and stops other sub-systems

## Call-return model
- A control model in software execution
- Manage flow of control between different program units (functions or procedures)
- How it works
	1. Calling unit invokes other program unit by making function call
	2. Control is transferred between caller and callee to perform specific task or completion
		- Once callee completes the task, control is returned to caller immediately following the original function call
- Top-down subroutine model
	- A structured approach for software design and development
	- Follows hierarchical organisation
		- Tasks are divided into smaller subtasks
		- Decomposition of task until all tasks become a simple task to be in the program code
		- Call return model enables control flow to move from higher level routine to a lower level routine and vice versa
			- Allows developer to break down complex task into smaller and manageable routines
				- Ease system implementation and testing process
					- Decomposed task can be implemented and tested independently
- Normally used in sequential systems
	- Refers to software systems that executes instruction in linear, sequential order (one after another)
		- Normally follows a well-defined sequence of operations
		- Flow of the control progresses from one instruction to to the next
	- In call return model
		- Functions called one by one
		- Output of a function is used as the input for the next function
		- Ensures each function completes all tasks before control is returned to calling functions
		- Sequence is maintained and correct execution order can be followed

## Manager model
- One system component is assigned as the system manager
	- It controls the **start**, the **stop**, and the **coordination** of other system processes
	- Used in concurrent systems
	- Can be implemented in sequential systems as a case statement
