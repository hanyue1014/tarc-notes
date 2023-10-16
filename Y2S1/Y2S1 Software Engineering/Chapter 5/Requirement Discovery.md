> Interact with stakeholder to discover requirements

## Source of info
- Stakeholders
- Documentation
- Similar system specification

## Viewpoint-oriented analysis
- An approach to ensure **broad stakeholder coverage** when discovering requirements
- Viewpoints are used to **classify** stakeholders and other sources of requirements
- Important to organise in hierarchy because in large systems there are huge number of viewpoints, hierarchy helps identify viewpoints in same branch and are likely to share common requirements
	- Ensures all viewpoints are covered
	- Decides a viewpoint is valid or not
- [[#Interactor Viewpoints]]
- [[#Indirect Viewpoints]]
- [[#Domain Viewpoints]]
- There may be other more specific types of viewpoints
	- Providers & receivers of system services
	- Other systems that interfaces directly with the system
	- Regulations and standards
	- Engineering viewpoints
	- Marketing viewpoints
	- etc

### Interactor Viewpoints
- People or other system that interact directly with the system
- Provides the detailed system requirements
	- System features
	- System interfaces
- Customers, staffs, database

### Indirect Viewpoints
- People who do not use the system but influences the requirements in some way
- Provides high level organisational requirements and constraints
- Manager, security staff, marketing staff

### Domain Viewpoints
- Domain characteristics and constraints
- UI standards, law compliance, communication standards

## Techniques for requirement discovery
- Interview
	- May miss essential information from open and closed questions
- Prototyping
- Scenario
	- Stakeholders usually find it easier to relate to real life examples
	- General scenarios
		- System and user expectation when scenario starts
		- Normal flow of events
		- What can go wrong, how to handle
		- Info on other activities that might occur at the same time
		- System state when scenario ends
	- Scenarios can be written in **text** + **diagrams**
- Ethnography (observation)
	- To understand social and organisational requirements
	- Helps discovering implicit system requirements
		- Actual instead of formal
	- Focuses on end user only