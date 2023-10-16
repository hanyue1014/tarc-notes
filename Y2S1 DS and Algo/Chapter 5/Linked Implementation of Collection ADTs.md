Topic: [[Y2S1 DS and Algo]]

- Exists because overhead due to shifting during add and remove operation
- Array size is fixed and is too inflexible
- Linked implementation allows 
	- Allocate space when we actually add the entry (`new`)
	- Deallocate space when we remove the entry (garbage collector collects objects that no longer has any variable that references it)
	- Adding and removing just adjust links
- Achieved via linking [[LinkedNodes]]
- [[LinkedList#Add Operation|Add]] and [[LinkedList#Remove Operation|remove]] operation, they all share same way
- [[LinkedList]]
- [[LinkedStack]]
- [[LinkedQueue]]