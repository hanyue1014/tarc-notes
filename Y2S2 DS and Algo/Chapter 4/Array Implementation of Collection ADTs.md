Topic: [[Y2S1 DS and Algo]]

## Implementing the collection ADTs with arrays
### Step 1: Create interface
- [[ListInterface]]
- [[StackInterface]]
- [[QueueInterface]]

### Step 2: Concrete class
- [[ArrayList]]
- [[ArrayStack]]
- [[ArrayQueue]]

## Iterators
- Iterator is an object that allows the traversal of a collection of the data, beginning with the first entry
- Normally implemented as an inner class
- It may be manipulated
	- Check whether next entry exists
	- Asked to advance to the next entry
	- Gives a reference to the current entry
	- Modify the list as traversing
- `java.util.Iterator`
	- `hasNext()`
	- `next()`
	- `remove()`

### Implementing inner class iterator
```java
public class List {
	public ListIter getIterator() { return new ListIter(); }
	private class ListIter implements java.util.Iterator {
		// override the methods
	}
}
```