> The \<T> represents a [[Java Generic]]
```java
public class ArrayList<T> implements ListInterface<T> {
	private T[] array;
	// length will act as the pointer to the last element as well
	private int length;
	private int cap;
	private static final int DEFAULT_CAP = 5; // create an array of len 5 by default

	public ArrayList() { this(DEFAULT_CAP); }
	public ArrayList(int cap) {
		this.array = (T[]) new Object[cap]; // T cannot be used to initialise anything because it is now known at compile time, so need to cast it, and it is perfectly safe because every class in java is a child of Object 
		this.length = 0;
		this.cap = cap;
	}

	// to add item into the list, we can simply add it to the back
	// I do pattern xia, cuz this defined in the ListInterface
	@override
	public boolean add(T newEntry) {
		// if the array is full, we create a new array and copy the old array to the new one
		if (this.length >= this.array.length) {
			// alrd at the end of the array, create new array
			T[] newA = (T[]) Object[this.array.length + this.cap];
			for (int i = 0; i < this.array.length; i++)
				newA[i] = this.array[i];
			this.array = newA;
		}
		this.array[this.length] = newEntry;
		this.length++;
		return true; // since we will expand array, always will success when adding items
	}

	// left eh method I lazy implement, here's the pseudocode
	/**
	 * If remove last item, just set it to null
	 * If remove item in front or middle, shift all the back item to the front by 1
	 */
}
```