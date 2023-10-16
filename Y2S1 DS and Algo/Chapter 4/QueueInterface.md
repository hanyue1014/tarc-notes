> The \<T> represents a [[Java Generic]] type
```java
public interface QueueInterface<T> {
	public abstract void enqueue(T newEntry);
	public abstract T dequeue();
	public abstract T getFront();
	public abstract boolean isEmpty();
	public abstract void clear();
}
```