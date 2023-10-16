- A paradigm that governs how software system handle and responds to events
- Flow of control is driven by events occurring at specific points in run time
	- User interactions
	- External signals
	- System notifications
	- Any other stuffs that requires the software to respond
- Each sub-system responds to externally generated events that might come from other sub-systems or environment

## Broadcast model
- Events that occur is broadcasted to all sub-systems
- Any sub-system that can handle the event may respond to it
- Effective in integrating sub-systems distributed across different computers on a network

## Interrupt driven model
- Used in real-time systems where interrupts are detected by an interrupt handler and passed to some other components after processing