> The \<T> represents a [[Java Generic]]
- Three types of implementations
	- Fixed Front (front index is fixed)
		- Good: Easy to understand
		- Bad: Need to shift all the elements to front every time dequeue (inefficient)
	- Dynamic Front (front index is not fixed)
		- Good: No need shift entries
		- Bad: Rightwards drift (when dequeue, the array's front part is not utilised)
	- Circular Array
		- How to check for empty and full
			- Use counter
			- Leave one empty space in array (this empty space will move along the array (not fixed in one place))
- Will just note down few methods worth mentioning
```java
// Fixed Front & dynamic front, backIndex starts from -1
public void enqueue() {
	if (this.backIndex < this.arr.length) {
		this.arr[this.backIndex++];
	}
}

// Fixed Front dequeue (for some reason my implementation diff with hers but this works as well, and don't need to store frontindex somemore)
public T dequeue() {
	// check, if queue isEmpty then quit, nothing to return also
	if (this.isEmpty()) return null;
	T temp = this.arr[0]; // front always is the first

	// shift the array
	for (int i = 1; i <= this.backIndex; i++) {
		this.arr[i - 1] = this.arr[i];
	}
	this.backIndex--;

	return temp;
}

// dynamic front dequeue
public T dequeue() {
	// check, if queue isEmpty then quit, nothing to return also
	if (this.isEmpty()) return null;
	T temp = this.arr[this.frontIndex];
	this.arr[this.frontIndex++] = null;
	return temp;
}

// Fixed Front isEmpty
public boolean isEmpty() {
	return this.backIndex < 0; // queue empty if backIndex is -1
}

// dynamic front isEmpty
public boolean isEmpty() {
	return this.frontIndex >= this.backIndex;
}

// circular array implementations, backIndex starts at the last element of the array, frontIndex starts at the first element of the array
// both use counter and leave empty space is same
public void enqueue(T newEntry) {
	if (this.isFull()) return;
	this.backIndex = (this.backIndex + 1) % this.arr.length;
	this.arr[this.backIndex] = newEntry;
	if (this.implementation == USE_COUNTER)
		this.counter++;
}

public T dequeue() {
	if (this.isEmpty()) return;
	T temp = this.arr[this.frontIndex];
	this.frontIndex = (this.frontIndex + 1) % this.arr.length;
	if (this.implementation == USE_COUNTER)
		this.counter--;
	return temp;
}

// use counter eh isEmpty and isFull
public boolean isEmpty() {
	return this.counter == 0;
}

public boolean isFull() {
	return this.counter == this.arr.length;
}

// leave one empty space eh isEmpty and isFull
public boolean isEmpty() {
	// if backIndex is one location in front, i.e front = 1, back = 0 / front = 0, back = 6 (wraparound, assume array length is 7)
	return (this.backIndex + 1) % this.arr.length == this.frontIndex;
}

public boolean isFull() {
	// if there is only one empty space left in the array
	// cuz the empty space will always be in between frontIndex and backIndex due to the implementation
	// so if we move backIndex 2 times and it reaches where the front index is, we know in between those two will always only be the empty space
	return (this.backIndex + 2) % this.arr.length == this.frontIndex;
}
```
