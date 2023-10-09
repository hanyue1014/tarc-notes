Topic: [[Y2S1 Software Engineering]]

## Foreword
- UI should be designed to match the skills, experience and expectations of its users
- System users often judge a system by its interface rather that its functionality
- Poorly designed interface can cause user to make errors
- Poor UI design is why so many software systems are never used
- Human factors in interface design
	- Limited short-term memory
		- Can instantaneously remember about 7 items of information
		- If more, more liable to make mistakes
	- People make mistakes
		- When mistakes were made, inappropriate alarms or messages increases stress and may cause even more mistakes
	- People are different
	- People have different interaction preferences

## UI Design Process
1. Analyse and understand user activities
2. Produce paper based design prototype
3. Evaluate design with end-users (can loop back to 2)
4. Produce dynamic design prototype
5. Evaluate design with end-users (can loop back to 4)
6. Implement final UI

## Common design issues
- System response time
- User help facilities
- Error information handling
- Command labeling

## Design modes
- Text-based
- [[GUI-based]]

## 3 Golden Rules for a good UI design
- Place user in control
	- People like to know the status of the system
- Reduce user's memory load
	- People have limited short-term memory
- Make the interface consistent
	- Easy to learn and knowledge learnt in one command or application is applicable to other parts of the system

## UI Design Principles
- User familiarity
	- Use terms and concepts drawn from experience of the end users
- Consistency
	- Operations should be activated in the same way for everywhere possible
- Minimal surprise
	- Never be surprised by the behaviour of a system
	- Eg. System suddenly fail
- Recoverability
	- Allow user to recover from errors
	- Eg. Undo function
- User guidance
	- Provide help facilities and meaningful error messages when errors occur
- User diversity
	- Provide appropriate interaction facilities for different types of users
	- Eg.
		- Provide step-by-step guidance for novice users
		- Shortcut key and advanced settings menu for expert users

## Key Issues in Interface Design
- How can user provide information to the computer system?
- How computer can present the information to the user?
- User provide information to computer system
	- Direct manipulation (eg. resizing graphic)
	- Menu selection
	- Command line
	- Natural Language
- Computer present information to the user
	- Data visualisation
		- Textual presentation
			- Customer details
		- Graphical presentation
			- Weather information shown as weather map
	- Color
		- Errors in using colors 
			- Using color to communicate meaning
				- Color-blinds may misinterpret
				- People has different perception of colors
			- Too many colors or colors too bright
				- Cause uncomfort
				- Cause confusion if colors are not used consistent
		- Guidance to use color
			- Use color change to denote change of status
			- Limit number of colors used
				- < 5 for a window
				- < 7 in an overall interface
			- Use color coding to support tasks the user trying to perform
				- Same color for similar tasks
			- Use color coding in a consistent way
				- If red was used for error messages, use red for all error messages
			- Color pairings
				- Some FG/BG combination can cause eyestrain and ineligible texts

## Message wording design factors
- Context
- Experience
- Skill level
- Style
- Culture

## Support Documentation for users
- Functional description
	- Description of services (used by system evaluators)
- Introductory manual
	- Getting started (beginner)
- System reference manual
	- Facility description (experienced users)
- System installation manual
	- How to install (system admin)
- System administrator manual
	- Operation and maintenance (system admin)