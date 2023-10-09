Topic: [[Y2S1 Software Engineering]]

## Foreword
- Reliability as an aspect of software quality
- Testing only demonstrates presence of errors, it cannot show that there are no errors in a program
- Testing should be scheduled as a part of the project planning process

## Why software testing (main goals)
- Validation testing
	- Demonstrate to the developer and customer that the software meets requirements
- Defect testing
	- Discover faults or defects in the software where the behaviour of the software may be incorrect, undesirable or does not conform to the specification

## Stages in software testing
- [[Unit Testing]]
- [[Module Testing]]
- [[Sub-system Testing]]
- [[System Testing]]
- [[Acceptance Testing]]

## Test data
- [[Live Data]]
- [[Artificial Data]]
- Test Library
	- Store all test data
	- Assure all systems are properly tested
	- A set of data developed to thoroughly test a system of programs

## Testing techniques
- [[Technique for Integration Testing]]
- [[Techniques for Black Box Testing]]
- [[Performance or Stress Test]]
- [[Testing Techniques for Unit Testing]]
- [[Other Testing Techniques]]

## Testing strategies
- A general approach to the testing process
- Not a method of devising particular system or component tests
- Techniques
	- Proactive
	- Reactive

## Test case design and planning
- Test planning -> set out standards for testing process
- Contents of test plan may include
	- Testing process
		- Type of test (unit testing, module testing etc)
	- Requirement traceability
		- SRS item x
	- Tested items
		- Program modules
		- User procedures
		- Operator procedures
	- Testing schedule
		- Gantt chart on the schedule to test each item
	- Testing recording procedures
	- Hardware and software requirements
	- Constraints
		- Test item availability
		- Test resource availability 
		- Time constraints

### Approaches for test case design
- Requirement-based testing
	- Test system requirements being met
- Partition testing
	- Identify input and output partitions to design tests so system executes input from all partitions and generate outputs in all partitions
- Structural testing
	- Use knowledge of program's structure to design tests to exercise all parts of program
	- Should try to execute each program statement at least once

## Testing principles / Guidelines
- All tests should be traceable to customer requirements
- Tests should be planned long before testing begins
	- Test plan can begin as soon as the requirement model is complete
	- Test cases can begin as soon as design model has been confirmed
- Pareto principle applies to software testing
	- 80% errors found during testing will likely be traceable to 20% of all program
	- Isolate suspected components and thoroughly test them
 - Test should begin in small and progress toward testing in the large
	 - Focus on individual components first
	 - Then find errors in integrated components
	 - Finally the entire system
 - Exhaustive testing is not possible
	 - Impossible to test every combination of paths during testing
 - To be effective, test should be conducted by an independent third party
	 - Developers might only test the parts that they personally think has defects