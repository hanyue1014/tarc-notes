> The \<T> represents a [[Java Generic]]
- There are two ways of implementing
	- Array's first element represent bottom of stack, last element represent stack's top
		- Avoids shifting elements of array (which is very heavy)
	- Array's first element represent top of stack
```java
// implementation one
public class ArrayStack<T> implements StackInterface<T> {
	private T[] arr;
	private int topIndex = -1; // signifies nothing is here yet

	// I am lazy, just fixed stack size idc
	public ArrayStack() { this.arr = (T[]) new Object[5]; }

	@override
	public boolean push(T newEntry) {
		this.arr[++this.topIndex] = newEntry;
	}

	@override
	public T pop() {
		T temp = this.arr[this.topIndex];
		this.arr[this.topIndex--] = null;
		return temp;
	}
}
```