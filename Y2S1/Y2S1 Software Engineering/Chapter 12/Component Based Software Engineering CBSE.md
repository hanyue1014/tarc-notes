Topic: [[Y2S1 Software Engineering]]

> Suitable for use if any components can be reused

## 4 Activities
- Component Qualification
	- Use a process of discovery and analysis to qualify each component's fit in the architecture and requirements
	- Factors
		- Function
		- Run-time requirements
		- Service requirements
		- Exception Handling
		- Security Features
- Component Adaptation
	- Change to meet architectural need
	- Remove architectural mismatches
	- Resolve Conflicts
	- White box wrapping
		- Code level modification
		- Not for Commercial Off The Shelf components
	- Grey box wrapping
		- Remove conflicts
		- Use API provided by component library
	- Black box wrapping
		- Preprocessing
		- Postprocessing
- Component Composition
	- Assemble all the components together
	- Infrastructure must be established to bind the components into operational system
- Component update
	- Occurs when requirement changed or new release

## Benefits
- Improved quality
- Increased productivity
- Save cost

## Obstacles
- Training
- More trouble than it's worth when reuse
- No incentive
- Not suitable for software development methodologies that don't facilitate reuse
